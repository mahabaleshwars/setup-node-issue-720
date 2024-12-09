A reproduction for <https://github.com/actions/setup-node/issues/720>.

[Actions](https://github.com/kevinoid/setup-node-issue-720/actions) hang on
step `actions/setup-node@v4` due to the presence of a non-empty file named
`node.js`. A 2 minute timeout is added to cause the workflow to fail after
waiting a reasonable amount of time.  The hang occurs due to
<https://github.com/npm/cmd-shim/issues/71>.
(Note: <https://github.com/npm/cmd-shim/pull/64> contains a possible fix.)
