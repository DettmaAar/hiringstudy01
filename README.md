Description:
You are contributing to the development of a pipeline to parse medical documents within an archive. All documents of a single patient are appended in one file in a random order. The documents can have the following origins: scans of printed documents (e.g. doctor letters, medication plans, printed lab results), scans of medical images (e.g. sonography-images or electrocardiograms [ECG]), programatically generated PDF-documents (e.g. letters, reports, lab reports, ECGs,  etc.) which were sent to the archive. It is possible that documents appear as single files (one document, single file) but it can also appear that a collection of paper documents (e..g 3 letters, lab results, medication plans) were scanned into one file and uploaded into a single file (multiple documents, single file).

Must-do task:
  - A function which takes a PDF file path as inputs and returns a dictionary which page has to be rotated by which angle to be upright (OCR-parsable). Documents can be generated PDFs (with embedded text) but are especially scanned pages. The documents may be landscape or portrait oriented.  The function is performant also for documents up to 200 pages.
  - A function which classifies pages of a 200 page document into 3 categories:
    1. machine-readable PDF / searchable PDF (e.g. internally generated discharge letter)
    2. Image-based PDF which may be OCR’d (e.g. discharge letters brought by the patient from an external hospital and then scanned)
    3. Image-based PDF which may not be OCR`d (e.g. ECG)
       
Cherry-on-the-cake task:
  - Provide a function which takes a filepath to a 200 page long PDF-file with mostly scanned and a few generated PDF documents. The file contains no index or table of contents. Your function has to return a list of extracted PDF pages which belong to one document, e.g. pages 1-3 extracted ⇒ doctor letter, page 4 ⇒ medication plan, pages 5-13 again a doctor’s letter, pages 13-21 another doctor’s letter.

A solution which will be considered contains at least:
  - Code (in your favorite programming language)
  - A sample document generated by yourself on which you developed your code
  - The returned outputs of your code in a machine readible format to be tested by our code
  - Is free of any malware
  - Uses less than 40GB VRAM GPU

Rating criteria:
- Functionality and adherence to the task description
- Performance (runtime, memory usage, GPU requirements)
- Dependence on third-party software / frameworks
- Code cleanliness, code documentation (e.g. DocString, Go Doc, rustdoc …)

  We are well aware that these tasks may require significant work. Aim to implement the best possible solution given the time and ressource constraints. 