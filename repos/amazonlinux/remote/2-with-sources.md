## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:1c2ff16aec2969b471271d267c5d3458c3a99fc8f584c410464de5e56a29d060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ae9a60bb771a5d7bae7d2b72be76465aa0fbba01798369693da7118683e76f8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.8 MB (476793057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edff84f869f5f2809dbcac4472a16c86a631e32be729065f187f37796636caf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 06:46:32 GMT
ADD file:119ae574c5d5b6e59e83ecadbe4c8dc4e7b535508e63704e74939df696c9b9a1 in / 
# Wed, 01 Apr 2020 06:46:33 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 06:47:00 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-4cda1b0d98865d12f61886af2ff052cf2cb4a48734bded0ac84d2664a0361220.tar.gz"  && echo "c53ef45b008bcb392f9ecbd229a6fa38f69cfe536d630560a8e1a8daaa8b68e6  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a8d577519c9fb37ef239a77026a16c019d20cce14b25867f57a44459b3bbf387`  
		Last Modified: Wed, 01 Apr 2020 06:48:00 GMT  
		Size: 61.7 MB (61655014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639485fb25df7e0bf5f7dfa45a2d1bf8980e990acd57646e3a7904ddbfd99ba3`  
		Last Modified: Wed, 01 Apr 2020 06:48:23 GMT  
		Size: 415.1 MB (415138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:20b1a9fe34ca33f2c1aacc4343fa97b0771d30ca2205167addab44c976fd726c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.2 MB (478210702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2dcdd719c4bfad05508a36c20f7d8100b941816a39367f4b3b4cedb6d39431`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 05:22:43 GMT
ADD file:40b8f329ad6d591029e1a4cde76c1d097315b136796d31bb9d3df35183423c14 in / 
# Wed, 01 Apr 2020 05:22:46 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 05:23:28 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-4cda1b0d98865d12f61886af2ff052cf2cb4a48734bded0ac84d2664a0361220.tar.gz"  && echo "c53ef45b008bcb392f9ecbd229a6fa38f69cfe536d630560a8e1a8daaa8b68e6  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:01d0a3bd5b98a6512409a10e5e5b065e87b794f924f3f9f7662939925aac631b`  
		Last Modified: Wed, 01 Apr 2020 05:24:01 GMT  
		Size: 63.1 MB (63072580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f5263e197d28b470047a0d5a85c7de9ceb69e2107bcc4eba8d080aef3bfa95`  
		Last Modified: Wed, 01 Apr 2020 05:24:46 GMT  
		Size: 415.1 MB (415138122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
