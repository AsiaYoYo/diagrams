```sequence
title rook ceph osd provision


cmd/rook/ceph/osd.go->cmd/rook/ceph/osd.go: 1. prepareOSD()
cmd/rook/ceph/osd.go->cmd/rook/ceph/osd.go: 2. getLocation()
cmd/rook/ceph/osd.go->pkg/operator/ceph/cluster/osd/osd.go: 3. GetLocationWithNode()
cmd/rook/ceph/osd.go->pkg/daemon/ceph/osd/agent.go: 4. NewAgent()
cmd/rook/ceph/osd.go->pkg/daemon/ceph/osd/daemon.go: 5. Provision()
pkg/daemon/ceph/osd/daemon.go->pkg/clusterd/disk.go: 6. DiscoverDevices()
pkg/daemon/ceph/osd/daemon.go->pkg/daemon/ceph/osd/daemon.go: 7. getAvailableDevices()
pkg/daemon/ceph/osd/daemon.go->pkg/daemon/ceph/osd/volume.go: 8. configureCVDevices()
pkg/daemon/ceph/osd/volume.go->pkg/daemon/ceph/osd/volume.go: 9. initializeDevices()
pkg/daemon/ceph/osd/daemon.go->pkg/operator/ceph/osd/status.go: 10. UpdateNodeStatus()
note right of pkg/operator/ceph/osd/status.go: Done.
```
