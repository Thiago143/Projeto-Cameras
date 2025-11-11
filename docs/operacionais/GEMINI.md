# Project Overview: "Projeto Câmeras 4º BPM"

This directory contains the planning, technical, and analytical documents for **"Projeto Câmeras 4º BPM"**. It is a proposed public-private partnership to implement an intelligent security monitoring system for the 4th Battalion of the Military Police of the State of Rio de Janeiro (PMERJ).

The project's goal is to create the "Ecossistema 4º BPM," an integrated system of 24/7 monitoring, intelligent analysis (including facial and behavioral detection), and real-time police response to improve public safety in the 4th Integrated Public Safety Area (AISP). The proposal emphasizes zero initial cost for the government, leveraging a private partner for equipment and infrastructure, with the police battalion managing the entire operation.

## Key Files

This is a non-code, documentation-based project. The main files are proposals, technical specifications, analyses, and visual assets.

*   **Executive Summary:**
    *   `sumario_executivo_cameras.pdf`: Provides a high-level overview of the project, including its justification, goals, innovative public-private partnership model, technical specifications, and expected outcomes. This is the best document to start with for a quick understanding.

*   **Technical & Implementation Documents:**
    *   `documento_tecnico_cameras.docx` / `documento_técnico_cameras.pdf`: The detailed technical document for the project.
    *   `especificacoes_tecnicas_A4.pdf`: Contains specific technical requirements for the hardware (cameras, etc.).
    *   `guia_implementacao_A4.pdf`: The guide detailing the steps for the project's implementation.

*   **Analytical Reports:**
    *   `Análises.pdf`: A general analysis document supporting the project.
    *   `impacto_dissuasao_criminal_A4.pdf`: A report on the expected impact of the camera system on criminal deterrence.

*   **Project Guidelines:**
    *   `AGENTS.md`: Contains important guidelines for managing the files in this repository, including naming conventions, how to "build" (i.e., export) documents, and security protocols.

*   **Visual Assets:**
    *   `Brasão_da_Polícia_Militar_do_Estado_do_Rio_de_Janeiro_-_PMERJ.png`, `brazao4.jpg`: Logos and visual assets for use in the documents.

## Usage and Development Conventions

This directory is used to store and manage all documentation related to the project. As outlined in `AGENTS.md`, there are specific conventions to follow:

*   **File Naming:** Files should follow a `topic_context_language.format` pattern (e.g., `sumario_executivo_cameras.pdf`). Suffixes like `_A4` or `_print` are used for derivatives.
*   **Document "Build" Process:** Since this is not a code project, "building" refers to converting source documents (like `.docx`) into distribution formats (like `.pdf`).
    *   **Example Conversion Command (macOS):**
        ```bash
        textutil -convert pdf documento_tecnico_cameras.docx
        ```
*   **Validation:** Before committing changes, contributors should check for conversion artifacts and validate layouts.
*   **Security:** All documents are considered sensitive. Raw footage or personal identifiers should not be committed. Image metadata should be stripped before committing.
    *   **Example Metadata Strip Command (macOS):**
        ```bash
        sips --stripImageMetadata brazao4.jpg
        ```
