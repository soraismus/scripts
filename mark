#!/bin/bash

# This script requires at least one argument (cmd).
# If 'cmd' doesn't exist, exit.
if [[ $# == 0 ]]; then
  echo "  This script requires at least one argument (cmd, ...optional-args)"
  exit 1;
fi

NAMESPACE="$(basename "$0")"
FN=$1
shift
ARGS="$@"

# Start a subshell, in which all of the functions of ...
# ... the namespace $NAMESPACE can be loaded.
# In the subshell, run the function $FN with args $ARGS.
bash -c "source $NAMESPACES/$NAMESPACE; $FN $ARGS"
