# bxBeaker

An experimental BoxLang property-testing POC using the `beaker(...).check(...)` API.

## Run the standalone POC

```bash
boxlang beaker-poc.bxs
```

## Run the TestBox spec

The TestBox checkout/install must include its runtime dependencies. Point `TESTBOX_HOME` at its root, then run:

```bash
TESTBOX_HOME=/path/to/TestBox boxlang --bx-config boxlang-testbox.json run-testbox-poc.bxs
```

`tests/specs/BeakerPropertySpec.bx` exercises multiple generated arguments, filtering, emails, arrays, nested structs, JSON, XML, fixed-seed replay, singleton generators, and failure reporting through TestBox. The test bundle defines local helper methods as stand-ins for the BIFs a future BoxLang module could register.

This POC does not implement shrinking or ship as a BoxLang module yet.
