# Roadmap
Pillar is mainly developed at the Blender Institute by a small team, with a
strong focus on project/asset management features. Our goal is to make Pillar
the foundation CMS for the studio pipeline.

## Home Project
We introduced
[Blender Sync](https://cloud.blender.org/blog/introducing-blender-sync) as first
iteration on the Home project, allowing users to synchronize their Blender
Startup and User Preferences files across multiple workstations, via the Blender
Cloud.

## Attract
We plan to reintegrate Attract into Pillar by creating specific Node Types, as
well as introducing the *application* property for a Node Type. Attract should
be developed as Pillar *module*, in an effort to keep the core application
generic and flexible.
Important extension will be made to the Blender Cloud addon (and to the Pillar
Python SDK) in order to allow interaction with Attract directly from Blender.

## Repository Node Types
A highly requested feature for Pillar is the support for VCS as a Node Type. The
idea is to create a Node Type that acts as interface for configuring (mostly
managing access) to Mercurial or SVN repository.
