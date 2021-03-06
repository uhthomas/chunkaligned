# chunkaligned
[![Build Status](https://travis-ci.org/wenjianhn/chunkaligned.png?branch=master)](https://travis-ci.org/wenjianhn/chunkaligned)
[![Coverage Status](https://coveralls.io/repos/wenjianhn/chunkaligned/badge.svg?branch=master)](https://coveralls.io/r/wenjianhn/chunkaligned?branch=master)

## Summary

NewChunkAlignedReaderAt returns a ReaderAt wrapper that is backed
by a ReaderAt r of size totalSize where the wrapper guarantees that
all ReadAt calls are aligned to chunkSize boundaries and of size
chunkSize (except for the final chunk, which may be shorter).

A chunk-aligned reader is good for caching, letting upper layers have
any access pattern, but guarantees that the wrapped ReaderAt sees
only nicely-cacheable access patterns & sizes.

## Usage

For API docs and examples, see tests.
