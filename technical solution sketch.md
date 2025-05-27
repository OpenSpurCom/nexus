# ACE - Automated Contribution Evaluation

Central to the architecture, this module evaluates the information density contributed by each user to the repo.
As you will see, modules are swapped based off what the majority adopts.
The specs can be found here:
The implementation will vary. 
What the community decides to use most will be the default for all modules. 

# Modules and dependencies(also modules)

Modules are the building blocks of the system.
These can be ideas or actual implementations.
Can be public or private repos - or a combination of both.
We can have a public repo outlining the components it levrages.
The components, which are also modules, can be a mixture of public and private implementations.

Modules have clear APIs the user can call and that they call grouped by module.
Dependencies have clear APIs as well, which make them swappable.

# Module registry

The module registry is a parallel registry to the default one we use nowadays.
Declaring a npm dependency will prompt the OpenSpur build machine to look for registered modules and swap the module at build time.
The module has an energy density measure attached and signed by the blockchain.

Modules compose the working software. 
During the build phase, the build machine computes an elliptic curve with keys by module authors which halts the execution after a certain amount of time. 

# Blockchain 

The blockchain handles payments and payment splitting and validates or invalidates build requests.

Users can pay to have their software assmbled by specifying the git repository they want to build.
The blockchain returns an invoice number and distributes the funds to the contributors.
The OpenSpur system is part of this distribution, earning a percentage on each software build. 

When a build is requested, the build tool checks with the blockchain if the invoice for building the software cartridge has been paid.
It then gives the go-ahead to the build tool to produce the software cartridge.

# Software build machine

The build machine parses an entry point repo and extracts dependencies from clear text in the git repository.
It then retrieves the dependencies and does the same for each.
If the module can't be found in the repository, it computes the information density and assigns percentages to each contributor.

It then proceeds to build the software using the instructions present - be it a GitHub Action, a Jenkins build script or otherwise.

You can find the GitHub action that builds OpenSpur modules here.

# Business opportunity finder

We have indexed all P/L statements of public companies so you can search for problems public companies might have.
You can then write a module spec that would solve it. 

# Module opportunity finder

An LLM indexing all OpenSpur repos, making them searchable so contributors or people looking to redefine how things are done can do so.

# People finder

If you are stuck or you have written the specs for a module you want others to write, this is the place to find and notify others you need help.