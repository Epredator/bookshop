It's a sample project implemented in BTP according to the best CAP standards: https://cap.cloud.sap/docs/

Many things can be done simply by providing cds add command. Instruction how to use the command you can find in official documentation: https://cap.cloud.sap/docs/tools/cds-cli#data

here you can find part of this instruction:
> cds --help

USAGE
    cds <command> [<args>]
    cds <src>  =  cds compile <src>
    cds        =  cds help

COMMANDS
    i | init        jump-start cds-based projects
    a | add         add a feature to an existing project
      | gen         generate models/data using a descriptive prompt [beta]
    m | import      add models from external sources
    c | compile     compile cds models to different outputs
    p | parse       parses given cds models
    s | serve       run your services in local server
    w | watch       run and restart on file changes
      | mock        call cds serve with mocked service
    r | repl        read-eval-event loop
    e | env         inspect effective configuration
    b | build       prepare for deployment
    d | deploy      deploy to databases
      | up          build and deploy your application to the cloud
    y | bind        bind application to remote services
      | debug       debug your application
      | subscribe   subscribe a tenant to a multitenant SaaS app
      | unsubscribe unsubscribe a tenant from a multitenant SaaS app
    l | login       login to extensible multitenant SaaS app
      | logout      logout from extensible multitenant SaaS app
      | pull        pull base model of extensible SaaS app
      | push        push extension to extensible SaaS app
    t | lint        run linter for env or model checks
    v | version     get detailed version information
      | completion  add/remove cli completion for cds commands
    ? | help        get detailed usage information

  Learn more about each command using:
  cds help <command> or
  cds <command> --help


  Use cds help <command> or cds <command> ? to get specific help:

> cds repl --help

SYNOPSIS
    cds repl [ <options> ]

    Launches into a read-eval-print-loop, an interactive playground to
    experiment with cds' JavaScript APIs. See documentation of Node.js'
    REPL for details at http://nodejs.org/api/repl.html

OPTIONS
    -r | --run <project>

      Runs a cds server from a given CAP project folder, or module name.
      You can then access the entities and services of the running server.
      It's the same as using the repl's builtin .run command.

    -u | --use <cds feature>

      Loads the given cds feature into the repl's global context. For example,
      if you specify xl it makes the cds.xl module's methods available.
      It's the same as doing {ref,val,xpr,...} = cds.xl within the repl.

EXAMPLES
    cds repl --run bookshop
    cds repl --run .
    cds repl --use cds.ql

SEE ALSO
    cds eval  to evaluate and execute JavaScript.
    


cds init
Use cds init to create new projects.

The simplest form creates a minimal Node.js project. For Java, use


cds init --java


In addition, you can add (most of) the project 'facets' from below right when creating the project. For example to create a project with a sample bookshop model and configuration for SAP HANA, use:


cds init --add sample,hana