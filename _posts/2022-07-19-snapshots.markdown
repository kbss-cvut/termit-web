---
title:  "Snapshots"
lang: en
categories: Documentation
excerpt: "Snapshots allows users to preserve vocabulary state in time."
---

[🇨🇿 Czech version]({{"/cs/dokumentace/snapshots" | relative_url}}){: .btn .btn--info}

Snapshots allows users to preserve vocabulary state in time.

Snapshot can be created by clicking Create snapshot button in vocabulary details.

{% include figure image_path="/assets/images/posts/documentation/snapshot-1.png" alt="Snapshot can be created by clicking Create snapshot button in vocabulary details." %}{: .post-image }

Vocabulary snapshot is ontologically both vocabulary and snapshot. It contains all tropes and relators as vocabulary plus relation to the original vocabulary and date and time in which was snapshot created.

Together with vocabulary snapshot are created snapshots of all terms from the vocabulary. Same as for vocabulary snapshot, term snapshot is both snapshot and term with relation to original term and vocabulary snapshot and containing date and time of snapshot creation (which is the same as vocabulary snapshot creation date and time).

{% include figure image_path="/assets/images/posts/documentation/snapshot-2.png" alt="Schema of snapshots." %}{: .post-image }

Create snapshot button creates also snapshots of all terms related to the terms from the original vocabulary and their vocabularies. Instead of links between terms, snapshot therefore contains links between term snapshots (which have link to their vocabulary snapshot) from the exact time when the snapshot was created.

Currently, TermIt does not allow users to discover snapshots, but it may be obtained through REST API service adding `/versions` to URL endpoint and attribute `at` with timestamp value according to the ISO 8601. Service returns last snapshot created before the selected timestamp.

`[SERVISE_URL]/rest/public/terms/[TERM_TITLE]/versions?namespace=[NAMESPACE]&at=2022-07-04T08:50:30Z`
