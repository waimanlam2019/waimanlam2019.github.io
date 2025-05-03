---
layout: post
title: "Possibilities of AI assisted Programming"
date: 2025-05-03 22:20:27 +0800
categories: blog 
---

Since ChatGPT has surged in popularity, many people have started to wonder: will it make programmers obsolete? I’d like to share my two cents on the topic. In short—senior developers can rest easy.

From what I’ve seen, even though ChatGPT can generate working programs based on prompts from non-technical users, the resulting code is often difficult to maintain. It can certainly take on the role of a junior developer, but it still needs supervision.

A few days ago, I asked ChatGPT to create a [JavaFX program](https://github.com/waimanlam2019/pdfsplit-forkjoinpool) for demonstration purposes. The program ran successfully, but when I examined the code, I noticed it was very inefficient.

Let’s take a look at the code:

        @Override
         protected void compute() {
             if ((endPage - startPage) <= THRESHOLD) {
                 try (PDDocument document = PDDocument.load(sourcePdf)) {
                     for (int i = startPage; i < endPage; i++) {
                         PDDocument singlePage = new PDDocument();
                         singlePage.addPage(document.getPage(i));
                         File outFile = new File(outputDir, "page_" + (i + 1) + ".pdf");
                         singlePage.save(outFile);
                         singlePage.close();
                     }
                 } catch (IOException e) {
                     e.printStackTrace();
                 }
             } else {
                 int mid = (startPage + endPage) / 2;
                 invokeAll(
                         new PdfSplitTask(sourcePdf, outputDir, startPage, mid),
                         new PdfSplitTask(sourcePdf, outputDir, mid, endPage)
                 );
             }
         }
     }


The program was intended to demonstrate ForkJoinPool, but ChatGPT had placed the logic that loads the PDF file into memory inside the concurrent section. Now, imagine the PDF file is 1000MB in size. If the program repeatedly loads 1000MB into memory during each task, it will quickly run out of memory. To fix this, I refactored the code by extracting the loading logic from the compute() method and made it a shared resource instead.

This one anecdotal experience illustrates a broader point: AI-assisted programming can be useful, but it still requires human oversight—especially from experienced developers.
