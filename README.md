byte_stream is a header-only template function library using C++11 variadic templates to perform simply serialization/deserialization of POD datatypes.

This is mostly a thought experiment and could likely be extended in various ways to be more useful, but it allows serialization of data to be used with MPI pretty easily which is most of what it is currently used for. The concept could be extended with a couple pure-virtual interface classes to provide common interfaces for serialization/deserialization to make moving POD (or deep-copy if any contained data members which are not POD also implement the interface) objects around using MPI very straightforward.