<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.1`](#registry281)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:8c51be2f669c82da8015017ff1eae5e5155fcf707ba914c5c7b798fbeb03b50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:7c8b70990dad7e4325bf26142f59f77c969c51e079918f4631767ac8d49e22fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9198989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db46f9d755043e6c427912d5c36b4375d68d31ab46ef9782fef06bdee1ed2cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 20:35:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 02:08:38 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 02:08:38 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 02:08:38 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 02:08:39 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 02:08:39 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 02:08:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 02:08:39 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d52c8ad3c485a42affe0f6bb1797d97df31a9900f74dca16b5a207487e58dd`  
		Last Modified: Wed, 29 Mar 2023 20:41:42 GMT  
		Size: 284.8 KB (284756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f80cd081c9c3756c8c0a5dfcef09be59bc25d88a86df04eb103a245970bbad`  
		Last Modified: Thu, 30 Mar 2023 02:08:48 GMT  
		Size: 6.1 MB (6105817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8951d7f653f0cfe7c4073a629f314cbbdbea8ed6d8824c26e662dcb3bea86a`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee46e9ce9b61c25cf42ca0f2f7b9ad6fbf38986bf5436ab56f283c6166c92ad`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:260cbc2791446c320c012702b4470c18c2cb5e004e4967b679ea7a4cb6d59e5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8572846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e5a4e419c424a3c972226142ea0473239d3b896005346c006f49de541f242b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:13:12 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 23:58:39 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 23:58:40 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 23:58:40 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 23:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 23:58:40 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61cd94d249d61c4970b0d9e3e62e7f3294fa96c87a6f69de03190e12f78079d`  
		Last Modified: Wed, 29 Mar 2023 19:21:12 GMT  
		Size: 284.7 KB (284710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bbe78bfdcd4d16faec151efd2fc1212fccc1df6dd1f6cb92fa43dcf38c63e2`  
		Last Modified: Wed, 29 Mar 2023 23:58:48 GMT  
		Size: 5.7 MB (5670677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97521397811c9a0f28445015bcfd4c545e3eb983c7c278b734c66edffb0a678`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5efe838e4e1e23f045ab951e44f009e3593a4e2019ecae1089931390ec9d3`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:4d24fa7dfcee0faab10e1b204d5f53c596ff4bdec49593d19cbd8f1cfdf1cf2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8370704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e7feed336a0c5d8f3deb897f2b88b8497a9d957e65e70aa1bee7a70af9b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:18:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 08 Apr 2023 02:48:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 08 Apr 2023 02:48:24 GMT
VOLUME [/var/lib/registry]
# Sat, 08 Apr 2023 02:48:24 GMT
EXPOSE 5000
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 08 Apr 2023 02:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Apr 2023 02:48:24 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e09b5f906611635ae71377bb2422dcad00ded6df847985eae9078b8dac5a41`  
		Last Modified: Thu, 30 Mar 2023 01:28:40 GMT  
		Size: 283.9 KB (283883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0153236b644b5714972b4b32ce3fb958088ec965d2566b2956ddf36ceaba48b9`  
		Last Modified: Sat, 08 Apr 2023 02:48:34 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec494754f212dc6daafca1cf9af5d2d914ef5f57e45ecf7b2c629609d043cb5a`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdafc4ca76f63ac5a239ea5a4cc94b3e92ab86e7ce73c3bef6c620539c08203e`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:52a534342446d6c634d1ac8d1360c93d869393da735431965e0af83503c666e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8539172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72dda82b7801531001ca833cfdead9ed70a4cb9892a920d753753b83a3847fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:00:09 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 05:43:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 05:43:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 05:43:46 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 05:43:47 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 05:43:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 05:43:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 05:43:47 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5145a9c19e2ac3fd2d3033fee8dc2e298f8a4232d8725619f8f81de9d876126b`  
		Last Modified: Thu, 30 Mar 2023 04:04:50 GMT  
		Size: 284.8 KB (284759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36e14ae70d8c1997bc19b7b251c8293aa721fdeaf2f8ce342a2a68da6e3057`  
		Last Modified: Thu, 30 Mar 2023 05:43:55 GMT  
		Size: 5.5 MB (5544456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9326efe1e4a3d3ab10a9f91aac9cdfbdca6cd77fe0620e0d77045a159b3fb`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544654b4f256a03556a6daf1c269176de4c112fb9e3da8de66b03eacf2a6d86a`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:0ebdd96e381029e14c9dfdb701d038141c58fcede634808b1a830b569dd4d050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8407335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef1433ecd455c776916ec3cc92d093194d4ee1797d49290db57c3dbbc9b45ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:05:53 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 04:05:56 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 04:05:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 04:05:56 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 04:05:57 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 04:05:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 04:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 04:05:58 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37951815fff1349f7c3ca11d2a7ab41dfde01705206be0e708b3b59df20c5b9d`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 286.8 KB (286771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291dff42d7774c06d5d645cfc805c9fffeb9a5b275af19d3847574c19fc1e69e`  
		Last Modified: Thu, 30 Mar 2023 04:06:10 GMT  
		Size: 5.3 MB (5315280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f2dc011314cccb15dbd69aa859ca474f0587d69eeaafd4bbbd83af8c0578fd`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a655d646733fa630f99d8bcc8ba40acdbc437db973923fabe2053ba6d9162`  
		Last Modified: Thu, 30 Mar 2023 04:06:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:29a75960ef76392ed5881b505248e67af01cc2070d6023d8cef73fc7d8b8120b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8690553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89b97f154a0b09474e7b3936cf84b03ef8bacb6e973097da0014f037f38a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 22:13:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 22:13:34 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 22:13:34 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 22:13:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 22:13:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0dcc52066ebc0c61c7345eac4fc4f60b935c1d13787dec5d6039bd00deee6`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 285.0 KB (284998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc980afa910c4bf6742b7c6762d2fc54130e31e7f6cfb02b571bbd15e7b83110`  
		Last Modified: Wed, 29 Mar 2023 22:13:47 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53afd310fa435f9be5235ebdf40bd405708b7c8a05a361e1d1b71527bd83ce9`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c4d475ea404646dfe52e72d8e2eab7d3d571396f58dd27770968652042909b`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8`

```console
$ docker pull registry@sha256:8c51be2f669c82da8015017ff1eae5e5155fcf707ba914c5c7b798fbeb03b50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:2.8` - linux; amd64

```console
$ docker pull registry@sha256:7c8b70990dad7e4325bf26142f59f77c969c51e079918f4631767ac8d49e22fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9198989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db46f9d755043e6c427912d5c36b4375d68d31ab46ef9782fef06bdee1ed2cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 20:35:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 02:08:38 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 02:08:38 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 02:08:38 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 02:08:39 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 02:08:39 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 02:08:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 02:08:39 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d52c8ad3c485a42affe0f6bb1797d97df31a9900f74dca16b5a207487e58dd`  
		Last Modified: Wed, 29 Mar 2023 20:41:42 GMT  
		Size: 284.8 KB (284756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f80cd081c9c3756c8c0a5dfcef09be59bc25d88a86df04eb103a245970bbad`  
		Last Modified: Thu, 30 Mar 2023 02:08:48 GMT  
		Size: 6.1 MB (6105817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8951d7f653f0cfe7c4073a629f314cbbdbea8ed6d8824c26e662dcb3bea86a`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee46e9ce9b61c25cf42ca0f2f7b9ad6fbf38986bf5436ab56f283c6166c92ad`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:260cbc2791446c320c012702b4470c18c2cb5e004e4967b679ea7a4cb6d59e5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8572846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e5a4e419c424a3c972226142ea0473239d3b896005346c006f49de541f242b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:13:12 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 23:58:39 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 23:58:40 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 23:58:40 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 23:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 23:58:40 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61cd94d249d61c4970b0d9e3e62e7f3294fa96c87a6f69de03190e12f78079d`  
		Last Modified: Wed, 29 Mar 2023 19:21:12 GMT  
		Size: 284.7 KB (284710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bbe78bfdcd4d16faec151efd2fc1212fccc1df6dd1f6cb92fa43dcf38c63e2`  
		Last Modified: Wed, 29 Mar 2023 23:58:48 GMT  
		Size: 5.7 MB (5670677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97521397811c9a0f28445015bcfd4c545e3eb983c7c278b734c66edffb0a678`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5efe838e4e1e23f045ab951e44f009e3593a4e2019ecae1089931390ec9d3`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:4d24fa7dfcee0faab10e1b204d5f53c596ff4bdec49593d19cbd8f1cfdf1cf2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8370704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e7feed336a0c5d8f3deb897f2b88b8497a9d957e65e70aa1bee7a70af9b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:18:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 08 Apr 2023 02:48:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 08 Apr 2023 02:48:24 GMT
VOLUME [/var/lib/registry]
# Sat, 08 Apr 2023 02:48:24 GMT
EXPOSE 5000
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 08 Apr 2023 02:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Apr 2023 02:48:24 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e09b5f906611635ae71377bb2422dcad00ded6df847985eae9078b8dac5a41`  
		Last Modified: Thu, 30 Mar 2023 01:28:40 GMT  
		Size: 283.9 KB (283883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0153236b644b5714972b4b32ce3fb958088ec965d2566b2956ddf36ceaba48b9`  
		Last Modified: Sat, 08 Apr 2023 02:48:34 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec494754f212dc6daafca1cf9af5d2d914ef5f57e45ecf7b2c629609d043cb5a`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdafc4ca76f63ac5a239ea5a4cc94b3e92ab86e7ce73c3bef6c620539c08203e`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:52a534342446d6c634d1ac8d1360c93d869393da735431965e0af83503c666e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8539172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72dda82b7801531001ca833cfdead9ed70a4cb9892a920d753753b83a3847fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:00:09 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 05:43:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 05:43:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 05:43:46 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 05:43:47 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 05:43:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 05:43:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 05:43:47 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5145a9c19e2ac3fd2d3033fee8dc2e298f8a4232d8725619f8f81de9d876126b`  
		Last Modified: Thu, 30 Mar 2023 04:04:50 GMT  
		Size: 284.8 KB (284759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36e14ae70d8c1997bc19b7b251c8293aa721fdeaf2f8ce342a2a68da6e3057`  
		Last Modified: Thu, 30 Mar 2023 05:43:55 GMT  
		Size: 5.5 MB (5544456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9326efe1e4a3d3ab10a9f91aac9cdfbdca6cd77fe0620e0d77045a159b3fb`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544654b4f256a03556a6daf1c269176de4c112fb9e3da8de66b03eacf2a6d86a`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:0ebdd96e381029e14c9dfdb701d038141c58fcede634808b1a830b569dd4d050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8407335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef1433ecd455c776916ec3cc92d093194d4ee1797d49290db57c3dbbc9b45ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:05:53 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 04:05:56 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 04:05:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 04:05:56 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 04:05:57 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 04:05:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 04:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 04:05:58 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37951815fff1349f7c3ca11d2a7ab41dfde01705206be0e708b3b59df20c5b9d`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 286.8 KB (286771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291dff42d7774c06d5d645cfc805c9fffeb9a5b275af19d3847574c19fc1e69e`  
		Last Modified: Thu, 30 Mar 2023 04:06:10 GMT  
		Size: 5.3 MB (5315280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f2dc011314cccb15dbd69aa859ca474f0587d69eeaafd4bbbd83af8c0578fd`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a655d646733fa630f99d8bcc8ba40acdbc437db973923fabe2053ba6d9162`  
		Last Modified: Thu, 30 Mar 2023 04:06:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:29a75960ef76392ed5881b505248e67af01cc2070d6023d8cef73fc7d8b8120b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8690553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89b97f154a0b09474e7b3936cf84b03ef8bacb6e973097da0014f037f38a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 22:13:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 22:13:34 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 22:13:34 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 22:13:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 22:13:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0dcc52066ebc0c61c7345eac4fc4f60b935c1d13787dec5d6039bd00deee6`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 285.0 KB (284998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc980afa910c4bf6742b7c6762d2fc54130e31e7f6cfb02b571bbd15e7b83110`  
		Last Modified: Wed, 29 Mar 2023 22:13:47 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53afd310fa435f9be5235ebdf40bd405708b7c8a05a361e1d1b71527bd83ce9`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c4d475ea404646dfe52e72d8e2eab7d3d571396f58dd27770968652042909b`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8.1`

```console
$ docker pull registry@sha256:8c51be2f669c82da8015017ff1eae5e5155fcf707ba914c5c7b798fbeb03b50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:2.8.1` - linux; amd64

```console
$ docker pull registry@sha256:7c8b70990dad7e4325bf26142f59f77c969c51e079918f4631767ac8d49e22fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9198989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db46f9d755043e6c427912d5c36b4375d68d31ab46ef9782fef06bdee1ed2cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 20:35:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 02:08:38 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 02:08:38 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 02:08:38 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 02:08:39 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 02:08:39 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 02:08:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 02:08:39 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d52c8ad3c485a42affe0f6bb1797d97df31a9900f74dca16b5a207487e58dd`  
		Last Modified: Wed, 29 Mar 2023 20:41:42 GMT  
		Size: 284.8 KB (284756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f80cd081c9c3756c8c0a5dfcef09be59bc25d88a86df04eb103a245970bbad`  
		Last Modified: Thu, 30 Mar 2023 02:08:48 GMT  
		Size: 6.1 MB (6105817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8951d7f653f0cfe7c4073a629f314cbbdbea8ed6d8824c26e662dcb3bea86a`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee46e9ce9b61c25cf42ca0f2f7b9ad6fbf38986bf5436ab56f283c6166c92ad`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:260cbc2791446c320c012702b4470c18c2cb5e004e4967b679ea7a4cb6d59e5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8572846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e5a4e419c424a3c972226142ea0473239d3b896005346c006f49de541f242b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:13:12 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 23:58:39 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 23:58:40 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 23:58:40 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 23:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 23:58:40 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61cd94d249d61c4970b0d9e3e62e7f3294fa96c87a6f69de03190e12f78079d`  
		Last Modified: Wed, 29 Mar 2023 19:21:12 GMT  
		Size: 284.7 KB (284710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bbe78bfdcd4d16faec151efd2fc1212fccc1df6dd1f6cb92fa43dcf38c63e2`  
		Last Modified: Wed, 29 Mar 2023 23:58:48 GMT  
		Size: 5.7 MB (5670677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97521397811c9a0f28445015bcfd4c545e3eb983c7c278b734c66edffb0a678`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5efe838e4e1e23f045ab951e44f009e3593a4e2019ecae1089931390ec9d3`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:4d24fa7dfcee0faab10e1b204d5f53c596ff4bdec49593d19cbd8f1cfdf1cf2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8370704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e7feed336a0c5d8f3deb897f2b88b8497a9d957e65e70aa1bee7a70af9b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:18:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 08 Apr 2023 02:48:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 08 Apr 2023 02:48:24 GMT
VOLUME [/var/lib/registry]
# Sat, 08 Apr 2023 02:48:24 GMT
EXPOSE 5000
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 08 Apr 2023 02:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Apr 2023 02:48:24 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e09b5f906611635ae71377bb2422dcad00ded6df847985eae9078b8dac5a41`  
		Last Modified: Thu, 30 Mar 2023 01:28:40 GMT  
		Size: 283.9 KB (283883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0153236b644b5714972b4b32ce3fb958088ec965d2566b2956ddf36ceaba48b9`  
		Last Modified: Sat, 08 Apr 2023 02:48:34 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec494754f212dc6daafca1cf9af5d2d914ef5f57e45ecf7b2c629609d043cb5a`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdafc4ca76f63ac5a239ea5a4cc94b3e92ab86e7ce73c3bef6c620539c08203e`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:52a534342446d6c634d1ac8d1360c93d869393da735431965e0af83503c666e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8539172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72dda82b7801531001ca833cfdead9ed70a4cb9892a920d753753b83a3847fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:00:09 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 05:43:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 05:43:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 05:43:46 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 05:43:47 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 05:43:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 05:43:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 05:43:47 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5145a9c19e2ac3fd2d3033fee8dc2e298f8a4232d8725619f8f81de9d876126b`  
		Last Modified: Thu, 30 Mar 2023 04:04:50 GMT  
		Size: 284.8 KB (284759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36e14ae70d8c1997bc19b7b251c8293aa721fdeaf2f8ce342a2a68da6e3057`  
		Last Modified: Thu, 30 Mar 2023 05:43:55 GMT  
		Size: 5.5 MB (5544456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9326efe1e4a3d3ab10a9f91aac9cdfbdca6cd77fe0620e0d77045a159b3fb`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544654b4f256a03556a6daf1c269176de4c112fb9e3da8de66b03eacf2a6d86a`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; ppc64le

```console
$ docker pull registry@sha256:0ebdd96e381029e14c9dfdb701d038141c58fcede634808b1a830b569dd4d050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8407335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef1433ecd455c776916ec3cc92d093194d4ee1797d49290db57c3dbbc9b45ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:05:53 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 04:05:56 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 04:05:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 04:05:56 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 04:05:57 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 04:05:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 04:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 04:05:58 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37951815fff1349f7c3ca11d2a7ab41dfde01705206be0e708b3b59df20c5b9d`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 286.8 KB (286771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291dff42d7774c06d5d645cfc805c9fffeb9a5b275af19d3847574c19fc1e69e`  
		Last Modified: Thu, 30 Mar 2023 04:06:10 GMT  
		Size: 5.3 MB (5315280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f2dc011314cccb15dbd69aa859ca474f0587d69eeaafd4bbbd83af8c0578fd`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a655d646733fa630f99d8bcc8ba40acdbc437db973923fabe2053ba6d9162`  
		Last Modified: Thu, 30 Mar 2023 04:06:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; s390x

```console
$ docker pull registry@sha256:29a75960ef76392ed5881b505248e67af01cc2070d6023d8cef73fc7d8b8120b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8690553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89b97f154a0b09474e7b3936cf84b03ef8bacb6e973097da0014f037f38a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 22:13:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 22:13:34 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 22:13:34 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 22:13:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 22:13:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0dcc52066ebc0c61c7345eac4fc4f60b935c1d13787dec5d6039bd00deee6`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 285.0 KB (284998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc980afa910c4bf6742b7c6762d2fc54130e31e7f6cfb02b571bbd15e7b83110`  
		Last Modified: Wed, 29 Mar 2023 22:13:47 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53afd310fa435f9be5235ebdf40bd405708b7c8a05a361e1d1b71527bd83ce9`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c4d475ea404646dfe52e72d8e2eab7d3d571396f58dd27770968652042909b`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:8c51be2f669c82da8015017ff1eae5e5155fcf707ba914c5c7b798fbeb03b50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:7c8b70990dad7e4325bf26142f59f77c969c51e079918f4631767ac8d49e22fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9198989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db46f9d755043e6c427912d5c36b4375d68d31ab46ef9782fef06bdee1ed2cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 20:35:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 02:08:38 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 02:08:38 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 02:08:38 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 02:08:39 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 02:08:39 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 02:08:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 02:08:39 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d52c8ad3c485a42affe0f6bb1797d97df31a9900f74dca16b5a207487e58dd`  
		Last Modified: Wed, 29 Mar 2023 20:41:42 GMT  
		Size: 284.8 KB (284756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f80cd081c9c3756c8c0a5dfcef09be59bc25d88a86df04eb103a245970bbad`  
		Last Modified: Thu, 30 Mar 2023 02:08:48 GMT  
		Size: 6.1 MB (6105817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8951d7f653f0cfe7c4073a629f314cbbdbea8ed6d8824c26e662dcb3bea86a`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee46e9ce9b61c25cf42ca0f2f7b9ad6fbf38986bf5436ab56f283c6166c92ad`  
		Last Modified: Thu, 30 Mar 2023 02:08:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:260cbc2791446c320c012702b4470c18c2cb5e004e4967b679ea7a4cb6d59e5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8572846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e5a4e419c424a3c972226142ea0473239d3b896005346c006f49de541f242b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:13:12 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 23:58:39 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 23:58:40 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 23:58:40 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 23:58:40 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 23:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 23:58:40 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61cd94d249d61c4970b0d9e3e62e7f3294fa96c87a6f69de03190e12f78079d`  
		Last Modified: Wed, 29 Mar 2023 19:21:12 GMT  
		Size: 284.7 KB (284710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bbe78bfdcd4d16faec151efd2fc1212fccc1df6dd1f6cb92fa43dcf38c63e2`  
		Last Modified: Wed, 29 Mar 2023 23:58:48 GMT  
		Size: 5.7 MB (5670677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97521397811c9a0f28445015bcfd4c545e3eb983c7c278b734c66edffb0a678`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5efe838e4e1e23f045ab951e44f009e3593a4e2019ecae1089931390ec9d3`  
		Last Modified: Wed, 29 Mar 2023 23:58:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:4d24fa7dfcee0faab10e1b204d5f53c596ff4bdec49593d19cbd8f1cfdf1cf2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8370704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e7feed336a0c5d8f3deb897f2b88b8497a9d957e65e70aa1bee7a70af9b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:18:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 08 Apr 2023 02:48:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 08 Apr 2023 02:48:24 GMT
VOLUME [/var/lib/registry]
# Sat, 08 Apr 2023 02:48:24 GMT
EXPOSE 5000
# Sat, 08 Apr 2023 02:48:24 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 08 Apr 2023 02:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Apr 2023 02:48:24 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e09b5f906611635ae71377bb2422dcad00ded6df847985eae9078b8dac5a41`  
		Last Modified: Thu, 30 Mar 2023 01:28:40 GMT  
		Size: 283.9 KB (283883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0153236b644b5714972b4b32ce3fb958088ec965d2566b2956ddf36ceaba48b9`  
		Last Modified: Sat, 08 Apr 2023 02:48:34 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec494754f212dc6daafca1cf9af5d2d914ef5f57e45ecf7b2c629609d043cb5a`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdafc4ca76f63ac5a239ea5a4cc94b3e92ab86e7ce73c3bef6c620539c08203e`  
		Last Modified: Sat, 08 Apr 2023 02:48:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:52a534342446d6c634d1ac8d1360c93d869393da735431965e0af83503c666e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8539172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72dda82b7801531001ca833cfdead9ed70a4cb9892a920d753753b83a3847fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:00:09 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 05:43:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 05:43:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 05:43:46 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 05:43:47 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 05:43:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 05:43:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 05:43:47 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5145a9c19e2ac3fd2d3033fee8dc2e298f8a4232d8725619f8f81de9d876126b`  
		Last Modified: Thu, 30 Mar 2023 04:04:50 GMT  
		Size: 284.8 KB (284759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36e14ae70d8c1997bc19b7b251c8293aa721fdeaf2f8ce342a2a68da6e3057`  
		Last Modified: Thu, 30 Mar 2023 05:43:55 GMT  
		Size: 5.5 MB (5544456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9326efe1e4a3d3ab10a9f91aac9cdfbdca6cd77fe0620e0d77045a159b3fb`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544654b4f256a03556a6daf1c269176de4c112fb9e3da8de66b03eacf2a6d86a`  
		Last Modified: Thu, 30 Mar 2023 05:43:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:0ebdd96e381029e14c9dfdb701d038141c58fcede634808b1a830b569dd4d050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8407335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef1433ecd455c776916ec3cc92d093194d4ee1797d49290db57c3dbbc9b45ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:05:53 GMT
RUN apk add --no-cache ca-certificates
# Thu, 30 Mar 2023 04:05:56 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 30 Mar 2023 04:05:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 30 Mar 2023 04:05:56 GMT
VOLUME [/var/lib/registry]
# Thu, 30 Mar 2023 04:05:57 GMT
EXPOSE 5000
# Thu, 30 Mar 2023 04:05:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 30 Mar 2023 04:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 04:05:58 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37951815fff1349f7c3ca11d2a7ab41dfde01705206be0e708b3b59df20c5b9d`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 286.8 KB (286771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291dff42d7774c06d5d645cfc805c9fffeb9a5b275af19d3847574c19fc1e69e`  
		Last Modified: Thu, 30 Mar 2023 04:06:10 GMT  
		Size: 5.3 MB (5315280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f2dc011314cccb15dbd69aa859ca474f0587d69eeaafd4bbbd83af8c0578fd`  
		Last Modified: Thu, 30 Mar 2023 04:06:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a655d646733fa630f99d8bcc8ba40acdbc437db973923fabe2053ba6d9162`  
		Last Modified: Thu, 30 Mar 2023 04:06:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:29a75960ef76392ed5881b505248e67af01cc2070d6023d8cef73fc7d8b8120b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8690553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89b97f154a0b09474e7b3936cf84b03ef8bacb6e973097da0014f037f38a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 29 Mar 2023 22:13:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 29 Mar 2023 22:13:34 GMT
VOLUME [/var/lib/registry]
# Wed, 29 Mar 2023 22:13:34 GMT
EXPOSE 5000
# Wed, 29 Mar 2023 22:13:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 29 Mar 2023 22:13:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 22:13:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0dcc52066ebc0c61c7345eac4fc4f60b935c1d13787dec5d6039bd00deee6`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 285.0 KB (284998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc980afa910c4bf6742b7c6762d2fc54130e31e7f6cfb02b571bbd15e7b83110`  
		Last Modified: Wed, 29 Mar 2023 22:13:47 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53afd310fa435f9be5235ebdf40bd405708b7c8a05a361e1d1b71527bd83ce9`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c4d475ea404646dfe52e72d8e2eab7d3d571396f58dd27770968652042909b`  
		Last Modified: Wed, 29 Mar 2023 22:13:46 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
