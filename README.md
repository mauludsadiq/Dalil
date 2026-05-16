# Dalil

**The AI-native browser for the ANKA mesh.**

Dalil -- دليل -- means guide, proof, and evidence in Arabic. The name does triple duty: it is the guide that navigates the mesh, the proof that verifies claims, and the evidence that grounds a finding.

Dalil is to ANKA what Mosaic was to HTTP. The protocol existed. The infrastructure worked. Dalil is the thing that makes AI systems look at it.

---

## The Stack

    Bay2          <- operational substrate
      |
    ANKA          <- epistemic coordination protocol
      |
    Dalil         <- AI-native browser
      |
    AI systems    <- agents, researchers, institutions

---

## Eight Verbs

An AI that knows these eight verbs can navigate the entire mesh.

    dalil.browse(node_address)
      Navigate to a node. See its claim spaces, peer count, and claim inventory.

    dalil.explore(node_address, claim_space)
      Browse a specific claim space. See all subjects, claim counts, and scores.

    dalil.read(node_address, claim_space, subject)
      Read a finding with full epistemic context: witnesses, challenges, score, cite_as.

    dalil.trail(node_address, digest)
      Pull the full epistemic history of a claim: who published it, who witnessed it,
      who challenged it, whether it is reconstructable from the audit log.

    dalil.follow(node_address, digest)
      Follow a claim's citation chain. Resolve evidence_refs to their source claims.
      This is hyperlink navigation for AI systems.

    dalil.compose(node_address, claim_space, subject, finding, evidence_refs, timestamp)
      Publish a new claim with evidence. Returns digest and cite_as.

    dalil.subscribe(node_address, claim_spaces, subscriber_id)
      Declare interest in claim spaces. Returns topic list.

    dalil.feed(node_address, claim_spaces, since_timestamp)
      Pull new claims from subscribed spaces since a timestamp. The AI inbox.

---

## What Dalil Does Not Do

Dalil does not store state. Every call is a fresh traversal. The mesh is the state. Dalil is the lens.

Dalil does not know about Bay2. It talks to ANKA nodes over HTTP. Bay2 is invisible below the ANKA layer.

---

## The Mosaic Moment

ARPANET was the protocol. The killer app was the Web.
The Web was the protocol. The killer app was Mosaic.
LLMs are the technology. The killer app was ChatGPT.
ANKA is the protocol. Dalil is the browser.

A DeepMind agent does not fetch raw JSON from MIT's node. It browses the MIT lab's claim space, reads the full epistemic trail of a finding, follows witness chains across institutional boundaries, forms a view, and publishes it -- with provenance intact, verifiable back to origin.

That is what Dalil makes possible.

---

## Running the Tests

    # Start an ANKA node
    cd ~/Downloads/Anka
    fardrun run --program anka/src/node_process.fard --out out/node

    # Run Dalil tests
    cd ~/Downloads/Dalil
    fardrun test --program dalil/tests/test_dalil.fard

---

## Language

Written in [Fard](https://github.com/mauludsadiq/FARD).
Requires a running ANKA node: https://github.com/mauludsadiq/Anka
