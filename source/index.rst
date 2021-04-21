.. BrainExDocs documentation master file, created by
   sphinx-quickstart on Wed Apr 21 13:04:47 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. role:: red

Welcome to BrainExDocs's documentation!
=======================================

About BrainEx
========================
BrainEx is a General Exploration System that implements DTW in exploring time series.

Quick Start
-----------

API Calls
-----------
Here we detail some of the most commonly used API calls in the BrainEx API.

gxe_utils.load
********************************
:API: **gxe_utils.load(file_or_path, feature_num, num_worker, use_spark, header, driver_mem, max_result_mem)**

Loads a existing **genexengine** that was saved to disk or create new one from a csv file.

**Parameters**
   * file_or_path: string
   * feature_num: int
   * num_worker: int
   * use_spark: boolean
   * header: None or int
   * driver_mem: int
   * max_result_mem: int

brainexengine.build
********************************
:API: **brainexengine.build(st, dist_type, loi, verbose)**

Build a **brainexengine** for future queries

**Parameters**
   * st: float. Similarity threshold
   * dist_type: string
   * loi: int or tuples of two ints. Length of interest
   * verbose: int 0 or 1

brainexengine.query
********************************
:API: **brainexengine.query(query, besk_k, id_filter, filter_mode, loi, exlude_same_id, overlap)**

Queries a built **brainexengine** for a query sequence.

**Parameters**
   * query: **Sequence** or **ndarray**
   * besk_k: int
   * id_filter: list of strings
   * filter_mode: string
   * loi: int or tuples of two ints
   * exclude_same_id: boolean
   * overlap: float between 0 and 1 (inclusive). **Default 1** Prevents found matches from overlapping with each other. Set to 0 to allow NO overlapping between found matches, set to 0.5 is to say that found matches should not overlap with each other for more than 50%, set to 1 (default) means any overlap is allowed.



.. note::  Advanced parameter will be documented in the docs for developers.


.. toctree::
   :maxdepth: 2
   :caption: Contents:



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
