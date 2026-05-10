# Graph Report - /Volumes/Mini Drive/ODF_project  (2026-05-11)

## Corpus Check
- Corpus is ~7,635 words - fits in a single context window. You may not need a graph.

## Summary
- 166 nodes · 235 edges · 15 communities detected
- Extraction: 86% EXTRACTED · 14% INFERRED · 0% AMBIGUOUS · INFERRED: 34 edges (avg confidence: 0.66)
- Token cost: 3,200 input · 1,800 output

## Community Hubs (Navigation)
- [[_COMMUNITY_App Entry & UI Core|App Entry & UI Core]]
- [[_COMMUNITY_Embedder Engine|Embedder Engine]]
- [[_COMMUNITY_Shortcut Manager|Shortcut Manager]]
- [[_COMMUNITY_File Indexer|File Indexer]]
- [[_COMMUNITY_Search Architecture Design|Search Architecture Design]]
- [[_COMMUNITY_AI Inference Stack|AI Inference Stack]]
- [[_COMMUNITY_File Utilities|File Utilities]]
- [[_COMMUNITY_Document Extraction Pipeline|Document Extraction Pipeline]]
- [[_COMMUNITY_EXE Build System|EXE Build System]]
- [[_COMMUNITY_Global Hotkey System|Global Hotkey System]]
- [[_COMMUNITY_UI Package Init|UI Package Init]]
- [[_COMMUNITY_Utils Package Init|Utils Package Init]]
- [[_COMMUNITY_Search Engine Package Init|Search Engine Package Init]]
- [[_COMMUNITY_File Opener Reference|File Opener Reference]]
- [[_COMMUNITY_NumPy Dependency|NumPy Dependency]]

## God Nodes (most connected - your core abstractions)
1. `SearchWindow` - 36 edges
2. `Embedder` - 17 edges
3. `FileIndexer` - 14 edges
4. `VectorSearch` - 13 edges
5. `VectorSearch` - 8 edges
6. `ShortcutManager` - 7 edges
7. `register_global_shortcut()` - 5 edges
8. `main()` - 4 edges
9. `open_file()` - 4 edges
10. `ODF — Offline Document Finder` - 4 edges

## Surprising Connections (you probably didn't know these)
- `Chunking Strategy (1000-char overlap)` --semantically_similar_to--> `RAG Concept (Retrieve-and-Rank)`  [INFERRED] [semantically similar]
  PROJECT_OVERVIEW.md → ODF/README.md
- `Semantic Search (Natural Language)` --semantically_similar_to--> `RAG Concept (Retrieve-and-Rank)`  [INFERRED] [semantically similar]
  PROJECT_OVERVIEW.md → ODF/README.md
- `Offline / Local-First Privacy Design` --semantically_similar_to--> `ODF README`  [INFERRED] [semantically similar]
  PROJECT_OVERVIEW.md → ODF/README.md
- `Offline Document Finder (ODF) A smart AI-powered desktop tool for semantic sear` --uses--> `SearchWindow`  [INFERRED]
  /Volumes/Mini Drive/ODF_project/ODF/main.py → /Volumes/Mini Drive/ODF_project/ODF/ui/search_window.py
- `Main entry point for the ODF application.` --uses--> `SearchWindow`  [INFERRED]
  /Volumes/Mini Drive/ODF_project/ODF/main.py → /Volumes/Mini Drive/ODF_project/ODF/ui/search_window.py

## Hyperedges (group relationships)
- **End-to-End Search Pipeline** — project_overview_searchwindow, project_overview_vectorsearch, project_overview_embedder, project_overview_chromadb [EXTRACTED 0.95]
- **Document Indexing Pipeline** — project_overview_fileindexer, project_overview_pdfminer, project_overview_pythondocx, project_overview_vectorsearch, project_overview_embedder, project_overview_chunking_strategy [EXTRACTED 0.93]
- **Offline AI Inference Stack** — project_overview_fastembed, project_overview_onnx_runtime, project_overview_baai_model [EXTRACTED 0.97]

## Communities

### Community 0 - "App Entry & UI Core"
Cohesion: 0.11
Nodes (6): main(), Offline Document Finder (ODF) A smart AI-powered desktop tool for semantic sear, Main entry point for the ODF application., open_file(), Open a file using the default system application.          Args:         file, SearchWindow

### Community 1 - "Embedder Engine"
Cohesion: 0.09
Nodes (17): Embedder, Document and Query Embedder Handles text embedding using FastEmbed for high-per, Get information about the currently loaded model., Initialize the embedder with FastEmbed.                  Args:             mo, Generate embeddings for multiple texts.                  Args:             te, Generate embedding for a single text.                  Args:             text, Get the dimension of the embedding vectors., Vector Search Engine Handles ChromaDB-based similarity search for document retr (+9 more)

### Community 2 - "Shortcut Manager"
Cohesion: 0.1
Nodes (18): list_active_shortcuts(), Global Shortcut Registration Handles global keyboard shortcuts for the applicat, Unregister the global shortcut.          Args:         hotkey (str): Hotkey c, Initialize the shortcut manager., Stop all keyboard shortcuts and listener., Get list of active shortcuts., Safely register global shortcut with fallback.          Args:         callbac, Register a global shortcut.                  Args:             hotkey (str): (+10 more)

### Community 3 - "File Indexer"
Cohesion: 0.13
Nodes (9): FileIndexer, File Indexer Scans folders and extracts content from PDF, DOCX, and TXT files u, Process a single file: extract text and metadata.         Designed to be called, Extract text content from a file based on its extension., Check if a folder should be skipped (system, hidden, dev envs)., Initialize the file indexer., Scans the folder and returns a list of supported files.         Useful for gett, Process a list of files in parallel (multiprocessing) and yield documents. (+1 more)

### Community 4 - "Search Architecture Design"
Cohesion: 0.12
Nodes (20): ChromaDB (Vector Database), Chunking Strategy (1000-char overlap), CustomTkinter UI Framework, 280ms Debounce Search Trigger, Hybrid Search Algorithm, Incremental Indexing (MD5-based), ODF — Offline Document Finder, Offline / Local-First Privacy Design (+12 more)

### Community 5 - "AI Inference Stack"
Cohesion: 0.25
Nodes (8): BAAI/bge-small-en-v1.5 Model, build_exe.py (PyInstaller Build Script), Embedder (FastEmbed wrapper), FastEmbed Library, ONNX Runtime, PyInstaller, Rationale: ONNX Runtime for CPU-only Inference, fastembed>=0.2.0

### Community 6 - "File Utilities"
Cohesion: 0.33
Nodes (5): get_file_info(), open_folder(), File Opener Utility Opens files using the default system application., Open a folder in the default file manager.          Args:         folder_path, Get basic information about a file.          Args:         file_path (str): P

### Community 7 - "Document Extraction Pipeline"
Cohesion: 0.33
Nodes (6): FileIndexer, pdfminer.six (PDF Extraction), python-docx (DOCX Extraction), ThreadPoolExecutor (Parallel Processing), pdfminer.six>=20220524, python-docx>=0.8.11

### Community 8 - "EXE Build System"
Cohesion: 0.67
Nodes (1): ODF Build Script Produces a single ODF.exe that anyone can double-click and run.

### Community 9 - "Global Hotkey System"
Cohesion: 0.67
Nodes (3): keyboard Library (Global Hotkey), ShortcutManager, keyboard (hotkey dependency)

### Community 10 - "UI Package Init"
Cohesion: 1.0
Nodes (0): 

### Community 11 - "Utils Package Init"
Cohesion: 1.0
Nodes (0): 

### Community 12 - "Search Engine Package Init"
Cohesion: 1.0
Nodes (0): 

### Community 13 - "File Opener Reference"
Cohesion: 1.0
Nodes (1): open_file.py (Cross-Platform Opener)

### Community 14 - "NumPy Dependency"
Cohesion: 1.0
Nodes (1): numpy>=1.21.0,<2.0.0

## Knowledge Gaps
- **47 isolated node(s):** `ODF Build Script Produces a single ODF.exe that anyone can double-click and run.`, `Global Shortcut Registration Handles global keyboard shortcuts for the applicat`, `Initialize the shortcut manager.`, `Register a global shortcut.                  Args:             hotkey (str):`, `Unregister a global shortcut.                  Args:             hotkey (str)` (+42 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `UI Package Init`** (1 nodes): `__init__.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Utils Package Init`** (1 nodes): `__init__.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Search Engine Package Init`** (1 nodes): `__init__.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `File Opener Reference`** (1 nodes): `open_file.py (Cross-Platform Opener)`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `NumPy Dependency`** (1 nodes): `numpy>=1.21.0,<2.0.0`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `SearchWindow` connect `App Entry & UI Core` to `Embedder Engine`, `File Indexer`?**
  _High betweenness centrality (0.224) - this node is a cross-community bridge._
- **Why does `VectorSearch` connect `Embedder Engine` to `App Entry & UI Core`, `File Indexer`?**
  _High betweenness centrality (0.140) - this node is a cross-community bridge._
- **Why does `FileIndexer` connect `File Indexer` to `App Entry & UI Core`, `Embedder Engine`?**
  _High betweenness centrality (0.098) - this node is a cross-community bridge._
- **Are the 5 inferred relationships involving `SearchWindow` (e.g. with `Offline Document Finder (ODF) A smart AI-powered desktop tool for semantic sear` and `Main entry point for the ODF application.`) actually correct?**
  _`SearchWindow` has 5 INFERRED edges - model-reasoned connections that need verification._
- **Are the 11 inferred relationships involving `Embedder` (e.g. with `VectorSearch` and `Vector Search Engine Handles ChromaDB-based similarity search for document retr`) actually correct?**
  _`Embedder` has 11 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `FileIndexer` (e.g. with `SearchWindow` and `ODF Search Window Spotlight-inspired UI: clean, minimal, two-panel layout.`) actually correct?**
  _`FileIndexer` has 3 INFERRED edges - model-reasoned connections that need verification._
- **Are the 4 inferred relationships involving `VectorSearch` (e.g. with `SearchWindow` and `ODF Search Window Spotlight-inspired UI: clean, minimal, two-panel layout.`) actually correct?**
  _`VectorSearch` has 4 INFERRED edges - model-reasoned connections that need verification._