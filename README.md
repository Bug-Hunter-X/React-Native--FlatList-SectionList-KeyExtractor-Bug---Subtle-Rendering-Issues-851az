# React Native FlatList/SectionList KeyExtractor Bug

This repository demonstrates a common, yet subtle, bug in React Native when using `FlatList` or `SectionList`.  The issue stems from an improperly configured `keyExtractor` prop, leading to unexpected rendering behavior.

## The Problem

When using `FlatList` or `SectionList`, providing a unique key for each item is crucial. If the keys aren't unique, React Native might struggle to efficiently update the list, causing incorrect rendering, data duplication, or performance issues.  Error messages are often not explicit and might manifest as seemingly random re-renders or items appearing in the wrong positions.

## Reproduction

The `bug.js` file contains a flawed implementation showing the incorrect use of `keyExtractor`.  Run the example to see the unexpected behavior.

## Solution

The `bugSolution.js` file provides the corrected implementation.  The key change is using a unique identifier from each data item as the key. This ensures that React Native can accurately track and update each item in the list.