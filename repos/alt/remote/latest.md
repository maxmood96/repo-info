## `alt:latest`

```console
$ docker pull alt@sha256:4fab03b8d23eb16147397b0bc41a5025ba59f4e834f7fb4b933ac5206431d740
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:1871dc35e256936b11da9b65bb093bd7d175c98b466a9eb504242189e29bad08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43995569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca237a6281300d66a9700d3416d3d30b82e40b2af342da00d7373d58ff8f7f6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 May 2024 15:35:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 03 May 2024 15:35:31 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Fri, 03 May 2024 15:35:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 03 May 2024 15:35:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ba6b8f73927b282c66153739a6b7474428b8c1a81e8a3f0f405c1d2eb1551156`  
		Last Modified: Sat, 04 May 2024 18:56:41 GMT  
		Size: 44.0 MB (43995377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5215fbebbe8ff3bb2236161c3ec4b4d5c846291a20c7668704c550b56e411509`  
		Last Modified: Mon, 08 Jul 2024 18:59:06 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:2ea935b030cfd424becf45f7f46f2c614c45e48df5199224822eeb87be8cd391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5a0b4faecd48fb6185f62fbb515160df329ecda3b6b95a807943aeeb3a4363`

```dockerfile
```

-	Layers:
	-	`sha256:828421eb48dea40fbac5eb1fb155cde6c33a286c5cf250fc2c641b8201d44675`  
		Last Modified: Mon, 08 Jul 2024 18:59:07 GMT  
		Size: 2.5 MB (2492915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4db1cf053a6e006c150a412cc62d69ab7efbcfee81fe5173a05fca4a18b25d`  
		Last Modified: Mon, 08 Jul 2024 18:59:06 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:522030a98fb30693115eff9c08f731ae7c18f74813211b13eb5e5c70b31cba94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267204736f5aef60b169379ea5fc7ea1c7548ec3ec44918249ce2344be066b0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 May 2024 15:35:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 03 May 2024 15:35:31 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Fri, 03 May 2024 15:35:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 03 May 2024 15:35:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fc2e0d37008027ce0163c808aa88a32086c30e953c23d916f71ee4315618340f`  
		Last Modified: Mon, 08 Jul 2024 19:08:49 GMT  
		Size: 43.2 MB (43213350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ea8838e78bca6434e65c9df6db614455465bc1ec9d22aa03a4ff55b9530251`  
		Last Modified: Mon, 08 Jul 2024 19:08:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:a9c0f0e8c2c29d674e5d561c79c9551e1bc1604bc4cfe58011277707247e0889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2497708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef29b878994ec97463c5c2e1da9d97886e1562968a19c639a8ddbbc5a8db7bc`

```dockerfile
```

-	Layers:
	-	`sha256:7e215df1ab88a41a74f3f018102c689b279989d01358f72480aef1a4d3dca9ae`  
		Last Modified: Mon, 08 Jul 2024 19:08:46 GMT  
		Size: 2.5 MB (2491566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d340c37935ae92ed974718b651302cfa1d99c468fd41b5db3a749511525fc96`  
		Last Modified: Mon, 08 Jul 2024 19:08:45 GMT  
		Size: 6.1 KB (6142 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:4dfb2f45bd884b5e5ba6c916255f95ea9de23b4d52f71b17a2a06ff6c0eda507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44686308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8aeba745b18e5bdf521be76757a459f7156cb67b48f2a70e30ff1f0f9254171`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 May 2024 15:35:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 03 May 2024 15:35:31 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Fri, 03 May 2024 15:35:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 03 May 2024 15:35:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:57fb39084584dbc7f57e6092e64f5bdf067d6bffe01587eef4c608311b2d4fbd`  
		Last Modified: Mon, 08 Jul 2024 18:58:59 GMT  
		Size: 44.7 MB (44686116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5d3958f34541c1a76519751bafdca4b14c99f58a66a5e0d71b13cbc578bdb2`  
		Last Modified: Mon, 08 Jul 2024 18:58:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:ac446099fbd349d463da152158b3c0f730fd668c973a0f1ae1bddc28b58c8d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5893268f503490767b59617901f7b402f0af94d70e88177202bcfec69326a59`

```dockerfile
```

-	Layers:
	-	`sha256:605bea838099b1e46f8a7dbaef956ab9eeeafc3268912f129c87a309e3b6dd9c`  
		Last Modified: Mon, 08 Jul 2024 18:58:58 GMT  
		Size: 2.5 MB (2494781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0368c198b10d60539a0d22bc8c503a2f1097bfd2b75cd144b92fbf0b0dc985b6`  
		Last Modified: Mon, 08 Jul 2024 18:58:58 GMT  
		Size: 6.1 KB (6072 bytes)  
		MIME: application/vnd.in-toto+json
