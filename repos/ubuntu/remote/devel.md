## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:3b7f6ef2485dd8e34da1fe788200663fe068d5c91150a9eccc21200d61cd77f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:3ea74abf68665a08418eb672d4b5a27810bf4c49fc8ab71d49072bc83adc2a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41623967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d855a6ab8006e94866584aa0cfcf3214e855e4aa66602b66a0ea1628e2b258e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jun 2026 04:12:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.9122.tar --tag 26.10
# Fri, 12 Jun 2026 04:12:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.entrypoint --clear=config.cmd
# Fri, 12 Jun 2026 04:12:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.cmd --config.cmd /bin/bash
# Fri, 12 Jun 2026 04:12:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jun 2026 04:12:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.labels --config.label org.opencontainers.image.version=26.10 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-12T04:12:03.949561+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:12:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.10 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-12T04:12:03.949561+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:12:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.control_data.9122.tar
```

-	Layers:
	-	`sha256:728c783aadfbe5149943488edc8d28bd143e929bf069f58f0c697254869d23ce`  
		Last Modified: Fri, 12 Jun 2026 06:07:07 GMT  
		Size: 41.6 MB (41623578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6036c33adc6226f90f2027fb94167fdc4df4f22d073104b10149ad04e874f90d`  
		Last Modified: Fri, 12 Jun 2026 06:07:10 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - unknown; unknown

```console
$ docker pull ubuntu@sha256:2f9b73b0d04df9421b3ae5934ddd6ab2e71a47e1c11e4466f02a11af2ce20df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6f501431faee4bfd45380956fa26099f11382a6e3c045bc0e0005d218656da`

```dockerfile
```

-	Layers:
	-	`sha256:9cf854b92a84d5c28fb8ac9b28116d4fb254ca73c2e2662553bcf21530708ab4`  
		Last Modified: Fri, 19 Jun 2026 00:31:23 GMT  
		Size: 3.7 MB (3710113 bytes)  
		MIME: application/vnd.in-toto+json

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:a9508f6d83c5a8beffd716b8f0d38aa5e331ac9fa9759d7200a71f0023caaf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38756175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0686335542e8c95c85d34b24052b2c270d72dae877f26eb998b925eae1a357d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jun 2026 04:14:05 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.9278.tar --tag 26.10
# Fri, 12 Jun 2026 04:14:06 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.entrypoint --clear=config.cmd
# Fri, 12 Jun 2026 04:14:06 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.cmd --config.cmd /bin/bash
# Fri, 12 Jun 2026 04:14:06 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jun 2026 04:14:06 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.labels --config.label org.opencontainers.image.version=26.10 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-12T04:14:06.976166+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:14:06 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.10 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-12T04:14:06.976166+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:14:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.control_data.9278.tar
```

-	Layers:
	-	`sha256:7f7272b36fbce7173e663d07c74e5fc41c54cb11dead3da913d27f1913ae3725`  
		Last Modified: Fri, 12 Jun 2026 06:06:56 GMT  
		Size: 38.8 MB (38755785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643ef4cc9fc07e4b8ecc6baf86eb3775e09deeefd9bae81d30c89cbf022b3780`  
		Last Modified: Fri, 12 Jun 2026 06:07:00 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - unknown; unknown

```console
$ docker pull ubuntu@sha256:daf153781aabaf23f7963aea83756d4fdbcde0a15dbc5fa90ea198b9e5cabae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd552eb5a61758237275267f899ac56c69aa69d7446e786342fb1d5dff1ddc2`

```dockerfile
```

-	Layers:
	-	`sha256:6082690a331f9581ce8e7459ae08400be87094c42e9e868d127c29857cd1df7e`  
		Last Modified: Fri, 19 Jun 2026 00:30:49 GMT  
		Size: 3.7 MB (3711492 bytes)  
		MIME: application/vnd.in-toto+json

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fc2889c291dfa614170f939d87501c5811132cae9a5a77a06cb9d5d4d6d10b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40773223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1ae40fece2d6aa003a365b24ad04d1b35fdc7a03f20982942f811c301a82d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jun 2026 04:13:59 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.9200.tar --tag 26.10
# Fri, 12 Jun 2026 04:14:00 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.entrypoint --clear=config.cmd
# Fri, 12 Jun 2026 04:14:00 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.cmd --config.cmd /bin/bash
# Fri, 12 Jun 2026 04:14:00 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jun 2026 04:14:00 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.labels --config.label org.opencontainers.image.version=26.10 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-12T04:14:00.043090+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:14:00 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.10 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-12T04:14:00.043090+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:14:00 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.control_data.9200.tar
```

-	Layers:
	-	`sha256:800060c3834ebd276ccc919800af70ce3bbc836a41c088298baf34546a21b604`  
		Last Modified: Fri, 12 Jun 2026 06:07:18 GMT  
		Size: 40.8 MB (40772836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2efbb6b8189ccf9a334732be9d933383c9158b409c62dc8a0c01ddfc271210c`  
		Last Modified: Fri, 12 Jun 2026 06:07:21 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - unknown; unknown

```console
$ docker pull ubuntu@sha256:2ebca1ba9daedaceccbbdfa401c9188f5015c11fde7f987a9a9a52f6fac01347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df37e9b749a0b707b120de798aabcfeaa747feca772e42aa5305c8837fb840b`

```dockerfile
```

-	Layers:
	-	`sha256:e093457930d3a94199563b887ff0af27f369f04940c224a9199dd8d4d09749d7`  
		Last Modified: Fri, 19 Jun 2026 00:31:06 GMT  
		Size: 3.7 MB (3710306 bytes)  
		MIME: application/vnd.in-toto+json

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a720b56aeffd436091c8d5523b547ef4785cb929cfa8e5064e1172deef8d4b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46653517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4969c3c01d81771f9602512dde78a1febb83949ab55a0b8b1da0389496fdf81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jun 2026 04:14:12 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.9157.tar --tag 26.10
# Fri, 12 Jun 2026 04:14:13 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.entrypoint --clear=config.cmd
# Fri, 12 Jun 2026 04:14:13 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.cmd --config.cmd /bin/bash
# Fri, 12 Jun 2026 04:14:13 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jun 2026 04:14:13 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.labels --config.label org.opencontainers.image.version=26.10 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-12T04:14:13.172530+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:14:13 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.10 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-12T04:14:13.172530+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:14:13 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.control_data.9157.tar
```

-	Layers:
	-	`sha256:42a42132f48896968af763bfca0890365d42c6f540a3460437c037f4518b085e`  
		Last Modified: Fri, 12 Jun 2026 06:07:38 GMT  
		Size: 46.7 MB (46653126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec384e4efa60ab75321502305716ca708c062a732d6231a326b435c580b50e3`  
		Last Modified: Fri, 12 Jun 2026 06:07:41 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - unknown; unknown

```console
$ docker pull ubuntu@sha256:3328f162e69bec5a7b69d010df5bae2615849ecadb78626b87f3eeac2d0c6508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68becbe32e2ff282b12c8072a279ec09721ff90a3577aea145de6c9c1a41cb3b`

```dockerfile
```

-	Layers:
	-	`sha256:629f802a974255d84dec358e81302a19017b2708dff934770551d071dad5afbe`  
		Last Modified: Fri, 19 Jun 2026 00:30:09 GMT  
		Size: 3.7 MB (3713640 bytes)  
		MIME: application/vnd.in-toto+json

### `ubuntu:devel` - linux; riscv64

```console
$ docker pull ubuntu@sha256:afa33b98a76c3442a34936e1088e0b870eb90b5af67f09e4295dee829fcae211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42320890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59c673d1b0a41b9593b9a472d4056f14c7ce09ee3fd00f8e9f573da1353cef5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 04:32:58 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4568.tar --tag 26.04
# Mon, 13 Apr 2026 04:33:07 GMT
RUN umoci config
# Mon, 13 Apr 2026 04:33:07 GMT
RUN umoci config
# Mon, 13 Apr 2026 04:33:07 GMT
RUN umoci config
# Mon, 13 Apr 2026 04:33:08 GMT
RUN umoci config
# Mon, 13 Apr 2026 04:33:08 GMT
RUN umoci config
# Mon, 13 Apr 2026 04:33:08 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4568.tar
```

-	Layers:
	-	`sha256:55aef9065811bddbbb1e034bc4fc4995b84c8d92a12dbec939f40bc5028abbb4`  
		Last Modified: Mon, 13 Apr 2026 04:43:27 GMT  
		Size: 42.3 MB (42320494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ca710c56d9293e21e482e90c3a6bfd6cdff5e1d92bf9e61a53fb83b46de9d4`  
		Last Modified: Mon, 13 Apr 2026 04:43:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - unknown; unknown

```console
$ docker pull ubuntu@sha256:ed3b548bda2b8a09935cbbdd2cfe48071f1bc8aa90c1b47f807e6055dbf63f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b375399e842dbaf1c3efc032e71a493fc5b9407bb173e07bc847f7f899725bfe`

```dockerfile
```

-	Layers:
	-	`sha256:ae8a84758f9a78d29a65ffa9d1fb51fc2f00a4af71d057d9cd06c8659ea14324`  
		Last Modified: Wed, 15 Apr 2026 20:29:52 GMT  
		Size: 3.6 MB (3620755 bytes)  
		MIME: application/vnd.in-toto+json

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:3e4a36ed1182a4671144990f7003e45f682a213153682b8f686843f39a9e89dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40988993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b0bb5be1884ebad9291d8be0dbd659fb23824a6944a98cf65b960de4a2a32b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jun 2026 04:16:19 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.9181.tar --tag 26.10
# Fri, 12 Jun 2026 04:16:19 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.entrypoint --clear=config.cmd
# Fri, 12 Jun 2026 04:16:19 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.cmd --config.cmd /bin/bash
# Fri, 12 Jun 2026 04:16:19 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jun 2026 04:16:19 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=config.labels --config.label org.opencontainers.image.version=26.10 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-12T04:16:19.882527+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:16:19 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.10 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-12T04:16:19.882527+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Fri, 12 Jun 2026 04:16:19 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/ubuntu:26.10 /home/buildd/rockcraft-ubuntu-75561fff66b354a13d64c0d043e5fb47/images/.temp_layer.control_data.9181.tar
```

-	Layers:
	-	`sha256:b6f1d866649b826033a409b2d594ef9a8c58cbf9ef333692a0416b2fc9ff8a4e`  
		Last Modified: Fri, 12 Jun 2026 06:07:49 GMT  
		Size: 41.0 MB (40988603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0b5969055c97723ae45059b0fd83202acea59ce17e813652c0812f821b3dca`  
		Last Modified: Fri, 12 Jun 2026 06:07:51 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - unknown; unknown

```console
$ docker pull ubuntu@sha256:3466371b18326b5e5855db5dc9f08009c4e5cb1f5f64a2af555780b23382509d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3712180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4529ee61f23ac19c9eca4f15854b8e66dbfbcbb70b13f6d888905c7854f6c140`

```dockerfile
```

-	Layers:
	-	`sha256:dde82d34d3463b1f10199e84ee0ac78ae5745e46413856b933bb0ce7ffe76e6f`  
		Last Modified: Fri, 19 Jun 2026 00:29:33 GMT  
		Size: 3.7 MB (3712180 bytes)  
		MIME: application/vnd.in-toto+json
