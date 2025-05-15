## `nats:latest`

```console
$ docker pull nats@sha256:3072e8ea890fe66b5921f75c1385b5f49b59a7f46171d697517d186830131fa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.7314; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 01 May 2025 10:59:08 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 01 May 2025 16:46:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 01 May 2025 16:46:51 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 01 May 2025 10:59:08 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 01 May 2025 16:46:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 01 May 2025 16:46:00 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 01 May 2025 10:59:11 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 01 May 2025 16:46:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 01 May 2025 16:46:03 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 01 May 2025 10:59:10 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 01 May 2025 16:46:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 01 May 2025 16:46:18 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 01 May 2025 10:59:10 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 01 May 2025 16:46:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 01 May 2025 16:46:32 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 01 May 2025 10:59:08 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 01 May 2025 16:48:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 01 May 2025 16:48:45 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
