<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.1`](#registry281)
-	[`registry:2.8.2-beta.2`](#registry282-beta2)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:dbaa3e69f563fc146f3337eb9de422f74f6765bf0203c891ddfbd74a6f9b56eb
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
$ docker pull registry@sha256:85d4cd48754d4e8e4d4fe933bbde017d969e0e20775507add9faca39064bf9b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9788612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5352b75f67e2e2df2bf2d96509248d1f618b8aa66d8b8c89d21e29111424881`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:10 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:11 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:12 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:12 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:12 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:12 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58116d8bf56953e5f30b7f50257c5bb2b5ba4aba460cb69f2ac57eea00aaa5dc`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f7fac5d815c6d815af9cd4a55d79c15f938c8b4dfbec0699b4155800cba752`  
		Last Modified: Wed, 10 May 2023 00:00:25 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe88d67f473ca63bdce57cf03a3e2ed2e201809c472970040b018f538a841789`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a19664cea732d19655fe73f24b0b3c22ddf2b51bb3fbb005ba651fb1febbcf`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:d002d4633b9d68ce336392e040ebd59a7ded522a3b479ed27068c7b1bc850601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9111855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff01fee827325890213929b64bc64d57bebe0e60798a5adb7745a95592c8165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:14 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:15 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:15 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:15 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:15 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a91154cf231582e0efd441a318760e357cccbcf664976f729d125fe63ccdc9`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 284.9 KB (284873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c865dcda756b3c78f5ed3ccb692d9e91d983a5bf4fa36351deff5fee6ec21ca1`  
		Last Modified: Tue, 09 May 2023 23:59:28 GMT  
		Size: 5.7 MB (5670689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40aa56ff6ea566e4022595c66d8d2f212fb790ccc5d167eddbb3d32e4b35ef71`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3e86673f0f8b7c433c179708f86adb1c4e3a774b7a03eeea9cc4844c3b5b46`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:da7bd08bbb9ff20403dcc1ecea6671c592536494f042393d218da481292699de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8861467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e4ff48c67c5c89f42c3252d77bcc3a814f923527a0fcb530062a7ef77b07a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:07:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:07:22 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:07:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:07:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:07:22 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:07:23 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:07:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:07:23 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7807d1567ad70e9e42db0b7a4aa54ab9afc3df1c31c3fb590ced28192601e947`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 284.1 KB (284075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eb023c6817a3b9fc48c3958a6d1a0a77c801d2803b75aa39237bf63c9a4fab`  
		Last Modified: Wed, 10 May 2023 00:07:36 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c68a60bbd4090f3c9e80eded44a78e4d66ed9f4b5ec431bc24ecc695d3d45`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae7d509d894975670d3fb6419ae740f2ed1f394bb11fc386dcf9db9701c564b`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:75182a34805c0e5b65b66c1a2702ca7392bf8e6319d7b638df3358fb60ee8a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9174198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e8344540f85b91a4c88972a2bd60223931511ef2bd5a4fbf65cd9149f0ec64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:03:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:03:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:03:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:03:34 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:03:34 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:03:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:03:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:03:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683203a1cdbff667eb41c5b6d8426e77bcb98ede7a1aaf8def0259eab83f01c`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 286.3 KB (286287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be85afcbc03b911e9fb6381ab096985863d6972399163ab7bc1bad5d744e415`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 5.5 MB (5544450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d211ac8fe2c79895180de976eb58b670c6b2f8ff29193c51ce52d0d9f2a6b30`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb7494219ddef2a0aeb7e5f5c952ec1f17a029677789977c171067bc436bd5b`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:606048bcc76d6ac565e5378e41b30d1447ab15e07cd05a617006f2c8745642ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8988190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04ec80703233aa9c104cc1dd3e85049bffc357feaafd0100fbf4e76ad5173e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:41 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:42 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:42 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:42 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376ba25ac41cec041d831e456ad293ec2efd7e4fd1357ae113210bfddd447a5f`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 286.7 KB (286653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21243f56c5e44c90b754e10c5b0101e1b0e71f3ce26255c2db38670818536cf`  
		Last Modified: Wed, 10 May 2023 00:00:01 GMT  
		Size: 5.3 MB (5315293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a5f39c1ca311071521e42d1025b4ade032b4bcbbeea140c62b46831bf83ce`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a628ae12d6f1c29427a7b657cda078084f20bc6d213b66e1836dd847d43875`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:3643cb1566457855bce020926ab2cf0397dd36e107705583d0bb283846eccb13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9059cff0d5eb82a211218ca2620baa870c6a9512496c6a98031ea0a6556b055`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:53 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:54 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:55 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:55 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:55 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:55 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:55 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72fc573296d33547281b8f37ff15a477a2844bdd1fff61bf191b5f18e14354`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 285.1 KB (285083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e188748775a448f897c6a25bfdce905cb74d8b7b0c0a1899a867bd3677db2f`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f887ef46f44c51c511fa48d46cdb0dfa53066f4aedc1790b598854cdeae91c2c`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26522c7f8863cd49e70bb220c4a24b383166089e129f7ce496feaf97100e317f`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8`

```console
$ docker pull registry@sha256:dbaa3e69f563fc146f3337eb9de422f74f6765bf0203c891ddfbd74a6f9b56eb
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
$ docker pull registry@sha256:85d4cd48754d4e8e4d4fe933bbde017d969e0e20775507add9faca39064bf9b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9788612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5352b75f67e2e2df2bf2d96509248d1f618b8aa66d8b8c89d21e29111424881`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:10 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:11 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:12 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:12 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:12 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:12 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58116d8bf56953e5f30b7f50257c5bb2b5ba4aba460cb69f2ac57eea00aaa5dc`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f7fac5d815c6d815af9cd4a55d79c15f938c8b4dfbec0699b4155800cba752`  
		Last Modified: Wed, 10 May 2023 00:00:25 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe88d67f473ca63bdce57cf03a3e2ed2e201809c472970040b018f538a841789`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a19664cea732d19655fe73f24b0b3c22ddf2b51bb3fbb005ba651fb1febbcf`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:d002d4633b9d68ce336392e040ebd59a7ded522a3b479ed27068c7b1bc850601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9111855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff01fee827325890213929b64bc64d57bebe0e60798a5adb7745a95592c8165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:14 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:15 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:15 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:15 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:15 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a91154cf231582e0efd441a318760e357cccbcf664976f729d125fe63ccdc9`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 284.9 KB (284873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c865dcda756b3c78f5ed3ccb692d9e91d983a5bf4fa36351deff5fee6ec21ca1`  
		Last Modified: Tue, 09 May 2023 23:59:28 GMT  
		Size: 5.7 MB (5670689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40aa56ff6ea566e4022595c66d8d2f212fb790ccc5d167eddbb3d32e4b35ef71`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3e86673f0f8b7c433c179708f86adb1c4e3a774b7a03eeea9cc4844c3b5b46`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:da7bd08bbb9ff20403dcc1ecea6671c592536494f042393d218da481292699de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8861467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e4ff48c67c5c89f42c3252d77bcc3a814f923527a0fcb530062a7ef77b07a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:07:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:07:22 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:07:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:07:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:07:22 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:07:23 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:07:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:07:23 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7807d1567ad70e9e42db0b7a4aa54ab9afc3df1c31c3fb590ced28192601e947`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 284.1 KB (284075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eb023c6817a3b9fc48c3958a6d1a0a77c801d2803b75aa39237bf63c9a4fab`  
		Last Modified: Wed, 10 May 2023 00:07:36 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c68a60bbd4090f3c9e80eded44a78e4d66ed9f4b5ec431bc24ecc695d3d45`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae7d509d894975670d3fb6419ae740f2ed1f394bb11fc386dcf9db9701c564b`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:75182a34805c0e5b65b66c1a2702ca7392bf8e6319d7b638df3358fb60ee8a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9174198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e8344540f85b91a4c88972a2bd60223931511ef2bd5a4fbf65cd9149f0ec64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:03:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:03:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:03:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:03:34 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:03:34 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:03:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:03:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:03:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683203a1cdbff667eb41c5b6d8426e77bcb98ede7a1aaf8def0259eab83f01c`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 286.3 KB (286287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be85afcbc03b911e9fb6381ab096985863d6972399163ab7bc1bad5d744e415`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 5.5 MB (5544450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d211ac8fe2c79895180de976eb58b670c6b2f8ff29193c51ce52d0d9f2a6b30`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb7494219ddef2a0aeb7e5f5c952ec1f17a029677789977c171067bc436bd5b`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:606048bcc76d6ac565e5378e41b30d1447ab15e07cd05a617006f2c8745642ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8988190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04ec80703233aa9c104cc1dd3e85049bffc357feaafd0100fbf4e76ad5173e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:41 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:42 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:42 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:42 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376ba25ac41cec041d831e456ad293ec2efd7e4fd1357ae113210bfddd447a5f`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 286.7 KB (286653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21243f56c5e44c90b754e10c5b0101e1b0e71f3ce26255c2db38670818536cf`  
		Last Modified: Wed, 10 May 2023 00:00:01 GMT  
		Size: 5.3 MB (5315293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a5f39c1ca311071521e42d1025b4ade032b4bcbbeea140c62b46831bf83ce`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a628ae12d6f1c29427a7b657cda078084f20bc6d213b66e1836dd847d43875`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:3643cb1566457855bce020926ab2cf0397dd36e107705583d0bb283846eccb13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9059cff0d5eb82a211218ca2620baa870c6a9512496c6a98031ea0a6556b055`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:53 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:54 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:55 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:55 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:55 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:55 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:55 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72fc573296d33547281b8f37ff15a477a2844bdd1fff61bf191b5f18e14354`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 285.1 KB (285083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e188748775a448f897c6a25bfdce905cb74d8b7b0c0a1899a867bd3677db2f`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f887ef46f44c51c511fa48d46cdb0dfa53066f4aedc1790b598854cdeae91c2c`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26522c7f8863cd49e70bb220c4a24b383166089e129f7ce496feaf97100e317f`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8.1`

```console
$ docker pull registry@sha256:dbaa3e69f563fc146f3337eb9de422f74f6765bf0203c891ddfbd74a6f9b56eb
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
$ docker pull registry@sha256:85d4cd48754d4e8e4d4fe933bbde017d969e0e20775507add9faca39064bf9b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9788612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5352b75f67e2e2df2bf2d96509248d1f618b8aa66d8b8c89d21e29111424881`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:10 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:11 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:12 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:12 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:12 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:12 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58116d8bf56953e5f30b7f50257c5bb2b5ba4aba460cb69f2ac57eea00aaa5dc`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f7fac5d815c6d815af9cd4a55d79c15f938c8b4dfbec0699b4155800cba752`  
		Last Modified: Wed, 10 May 2023 00:00:25 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe88d67f473ca63bdce57cf03a3e2ed2e201809c472970040b018f538a841789`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a19664cea732d19655fe73f24b0b3c22ddf2b51bb3fbb005ba651fb1febbcf`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:d002d4633b9d68ce336392e040ebd59a7ded522a3b479ed27068c7b1bc850601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9111855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff01fee827325890213929b64bc64d57bebe0e60798a5adb7745a95592c8165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:14 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:15 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:15 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:15 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:15 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a91154cf231582e0efd441a318760e357cccbcf664976f729d125fe63ccdc9`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 284.9 KB (284873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c865dcda756b3c78f5ed3ccb692d9e91d983a5bf4fa36351deff5fee6ec21ca1`  
		Last Modified: Tue, 09 May 2023 23:59:28 GMT  
		Size: 5.7 MB (5670689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40aa56ff6ea566e4022595c66d8d2f212fb790ccc5d167eddbb3d32e4b35ef71`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3e86673f0f8b7c433c179708f86adb1c4e3a774b7a03eeea9cc4844c3b5b46`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:da7bd08bbb9ff20403dcc1ecea6671c592536494f042393d218da481292699de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8861467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e4ff48c67c5c89f42c3252d77bcc3a814f923527a0fcb530062a7ef77b07a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:07:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:07:22 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:07:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:07:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:07:22 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:07:23 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:07:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:07:23 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7807d1567ad70e9e42db0b7a4aa54ab9afc3df1c31c3fb590ced28192601e947`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 284.1 KB (284075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eb023c6817a3b9fc48c3958a6d1a0a77c801d2803b75aa39237bf63c9a4fab`  
		Last Modified: Wed, 10 May 2023 00:07:36 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c68a60bbd4090f3c9e80eded44a78e4d66ed9f4b5ec431bc24ecc695d3d45`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae7d509d894975670d3fb6419ae740f2ed1f394bb11fc386dcf9db9701c564b`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:75182a34805c0e5b65b66c1a2702ca7392bf8e6319d7b638df3358fb60ee8a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9174198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e8344540f85b91a4c88972a2bd60223931511ef2bd5a4fbf65cd9149f0ec64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:03:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:03:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:03:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:03:34 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:03:34 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:03:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:03:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:03:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683203a1cdbff667eb41c5b6d8426e77bcb98ede7a1aaf8def0259eab83f01c`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 286.3 KB (286287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be85afcbc03b911e9fb6381ab096985863d6972399163ab7bc1bad5d744e415`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 5.5 MB (5544450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d211ac8fe2c79895180de976eb58b670c6b2f8ff29193c51ce52d0d9f2a6b30`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb7494219ddef2a0aeb7e5f5c952ec1f17a029677789977c171067bc436bd5b`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; ppc64le

```console
$ docker pull registry@sha256:606048bcc76d6ac565e5378e41b30d1447ab15e07cd05a617006f2c8745642ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8988190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04ec80703233aa9c104cc1dd3e85049bffc357feaafd0100fbf4e76ad5173e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:41 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:42 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:42 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:42 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376ba25ac41cec041d831e456ad293ec2efd7e4fd1357ae113210bfddd447a5f`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 286.7 KB (286653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21243f56c5e44c90b754e10c5b0101e1b0e71f3ce26255c2db38670818536cf`  
		Last Modified: Wed, 10 May 2023 00:00:01 GMT  
		Size: 5.3 MB (5315293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a5f39c1ca311071521e42d1025b4ade032b4bcbbeea140c62b46831bf83ce`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a628ae12d6f1c29427a7b657cda078084f20bc6d213b66e1836dd847d43875`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; s390x

```console
$ docker pull registry@sha256:3643cb1566457855bce020926ab2cf0397dd36e107705583d0bb283846eccb13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9059cff0d5eb82a211218ca2620baa870c6a9512496c6a98031ea0a6556b055`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:53 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:54 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:55 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:55 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:55 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:55 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:55 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72fc573296d33547281b8f37ff15a477a2844bdd1fff61bf191b5f18e14354`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 285.1 KB (285083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e188748775a448f897c6a25bfdce905cb74d8b7b0c0a1899a867bd3677db2f`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f887ef46f44c51c511fa48d46cdb0dfa53066f4aedc1790b598854cdeae91c2c`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26522c7f8863cd49e70bb220c4a24b383166089e129f7ce496feaf97100e317f`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8.2-beta.2`

```console
$ docker pull registry@sha256:5f7b60201e08733a3f273334ffc3ae5e62353b85c021829cfe6efe2c40a9cba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:2.8.2-beta.2` - linux; amd64

```console
$ docker pull registry@sha256:0f3f4ad2b64a178e0896f63bada1f2c9135a4a0f92406e093925fff35208449b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9591016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4177366af1585114113c96e36c8411983055c663dab3a78dc0c80d2939e17e08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:10 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:15 GMT
RUN set -eux; 	version='2.8.2-beta.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f16957fe46a797439892bcea255c9e98477b47a56e03df4906e920eb2db57c28' ;; 		aarch64) arch='arm64';   sha256='f1c713711bf547185b82139bb4413b0409a6849be918dc29ea08ec04a6f72806' ;; 		armhf)   arch='armv6';   sha256='364d4da480737627849892e4656bccdda4370007fac655b02e0c3cebe87e14a6' ;; 		armv7)   arch='armv7';   sha256='e989455bd142736873fbd77ea6e574a079958644527d8716e381fc6545a91a8a' ;; 		ppc64le) arch='ppc64le'; sha256='377f0f56d4a9eab32630856a6357b245d89050137e433b538c35aafc3b713580' ;; 		s390x)   arch='s390x';   sha256='66f63e84d7adf02d0b7d8a821c618c464970de3d1726dd1a13c2149a71798f53' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:16 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:16 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:16 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:16 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58116d8bf56953e5f30b7f50257c5bb2b5ba4aba460cb69f2ac57eea00aaa5dc`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a682f8f991b8fe4ab2237f3a9b74891edf9a74724ddb4a8a528c23693e6c6`  
		Last Modified: Wed, 10 May 2023 00:00:38 GMT  
		Size: 5.9 MB (5908224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ef7aa7a2708433d079d656b5f8a7439e54264428287e37d9c624a4f6ff5f4`  
		Last Modified: Wed, 10 May 2023 00:00:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48141448230586fe1a3fb73ae0c2ef4484dcf0d5411433b67bd3840ff06170dd`  
		Last Modified: Wed, 10 May 2023 00:00:36 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.2-beta.2` - linux; arm variant v6

```console
$ docker pull registry@sha256:64b013bac264867aa75f8ac1df0438512d3bab8eca7572a2c1197582544297c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9011292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93304ec8c70d2b3d8623e0d89c9534c365834fd88a5fc7bbbacfc66a1faa8292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:18 GMT
RUN set -eux; 	version='2.8.2-beta.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f16957fe46a797439892bcea255c9e98477b47a56e03df4906e920eb2db57c28' ;; 		aarch64) arch='arm64';   sha256='f1c713711bf547185b82139bb4413b0409a6849be918dc29ea08ec04a6f72806' ;; 		armhf)   arch='armv6';   sha256='364d4da480737627849892e4656bccdda4370007fac655b02e0c3cebe87e14a6' ;; 		armv7)   arch='armv7';   sha256='e989455bd142736873fbd77ea6e574a079958644527d8716e381fc6545a91a8a' ;; 		ppc64le) arch='ppc64le'; sha256='377f0f56d4a9eab32630856a6357b245d89050137e433b538c35aafc3b713580' ;; 		s390x)   arch='s390x';   sha256='66f63e84d7adf02d0b7d8a821c618c464970de3d1726dd1a13c2149a71798f53' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:18 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:18 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:19 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:19 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:19 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a91154cf231582e0efd441a318760e357cccbcf664976f729d125fe63ccdc9`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 284.9 KB (284873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0210f1c6e20a1b5211aff282bfabdf42431a2aced08c9644b1ff2c28c33d7c3`  
		Last Modified: Tue, 09 May 2023 23:59:40 GMT  
		Size: 5.6 MB (5570128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9534dffd43ae6f59777d5843dac9f7535e014827e5ee9475ddb439f78aca788`  
		Last Modified: Tue, 09 May 2023 23:59:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40088b1a063cb1bacb0b837dfeeb74f616277e4f13daefb965f52895bd7f1c59`  
		Last Modified: Tue, 09 May 2023 23:59:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.2-beta.2` - linux; arm variant v7

```console
$ docker pull registry@sha256:6415d80cb867e44996233af8e8f9394bebaeebf7d6650e6cf04c9b37e23500ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8764982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a75c7c564c716aa2d80537daa0f455b41c8375a8d8393bd23f2239d0e11807`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:07:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:07:26 GMT
RUN set -eux; 	version='2.8.2-beta.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f16957fe46a797439892bcea255c9e98477b47a56e03df4906e920eb2db57c28' ;; 		aarch64) arch='arm64';   sha256='f1c713711bf547185b82139bb4413b0409a6849be918dc29ea08ec04a6f72806' ;; 		armhf)   arch='armv6';   sha256='364d4da480737627849892e4656bccdda4370007fac655b02e0c3cebe87e14a6' ;; 		armv7)   arch='armv7';   sha256='e989455bd142736873fbd77ea6e574a079958644527d8716e381fc6545a91a8a' ;; 		ppc64le) arch='ppc64le'; sha256='377f0f56d4a9eab32630856a6357b245d89050137e433b538c35aafc3b713580' ;; 		s390x)   arch='s390x';   sha256='66f63e84d7adf02d0b7d8a821c618c464970de3d1726dd1a13c2149a71798f53' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:07:26 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:07:26 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:07:26 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:07:26 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:07:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:07:27 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7807d1567ad70e9e42db0b7a4aa54ab9afc3df1c31c3fb590ced28192601e947`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 284.1 KB (284075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938ab52286acaca777e20984307baefad330c37cba376bfd5acb65614cda520`  
		Last Modified: Wed, 10 May 2023 00:07:49 GMT  
		Size: 5.6 MB (5569178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e42fd5df0a4e11992c753969112ec1782a7b509181c9694acf27e76f5e9181`  
		Last Modified: Wed, 10 May 2023 00:07:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbcb454da7a76e5aa3d1a3ce0e848bf0243624715d5472406dd7dff316c8730`  
		Last Modified: Wed, 10 May 2023 00:07:48 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.2-beta.2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:e060d7ea629fce0f06e78567e0b4016e41a329813bea28f24f0e27f2ba87cff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9013804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddc770ed61c366c0893e5cd488d37ca63b2eb1a101356d082db0a3777f3f3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:03:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:03:37 GMT
RUN set -eux; 	version='2.8.2-beta.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f16957fe46a797439892bcea255c9e98477b47a56e03df4906e920eb2db57c28' ;; 		aarch64) arch='arm64';   sha256='f1c713711bf547185b82139bb4413b0409a6849be918dc29ea08ec04a6f72806' ;; 		armhf)   arch='armv6';   sha256='364d4da480737627849892e4656bccdda4370007fac655b02e0c3cebe87e14a6' ;; 		armv7)   arch='armv7';   sha256='e989455bd142736873fbd77ea6e574a079958644527d8716e381fc6545a91a8a' ;; 		ppc64le) arch='ppc64le'; sha256='377f0f56d4a9eab32630856a6357b245d89050137e433b538c35aafc3b713580' ;; 		s390x)   arch='s390x';   sha256='66f63e84d7adf02d0b7d8a821c618c464970de3d1726dd1a13c2149a71798f53' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:03:37 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:03:37 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:03:37 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:03:37 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:03:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:03:38 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683203a1cdbff667eb41c5b6d8426e77bcb98ede7a1aaf8def0259eab83f01c`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 286.3 KB (286287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c9db8a3f12b117185678caf37ab6cf567adbd762336b16b7aa9184a5b06e4d`  
		Last Modified: Wed, 10 May 2023 00:03:59 GMT  
		Size: 5.4 MB (5384058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824d306038ac15df547c03e6f77860e7b25eef90eac48caa4c2ada54db301c9f`  
		Last Modified: Wed, 10 May 2023 00:03:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1878a90009bc6d7dfc5e14c4f1cd0a0e29f05e6f705e039689cf47b1548d34`  
		Last Modified: Wed, 10 May 2023 00:03:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.2-beta.2` - linux; ppc64le

```console
$ docker pull registry@sha256:79cb341d56e466d8d5ec51bec58da4ad7a6192a53e0ec872e0948078023ec069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8916736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96247b6ad70c547792195a9ac21959ea9df37847af484506614d817ae1ecc925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:48 GMT
RUN set -eux; 	version='2.8.2-beta.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f16957fe46a797439892bcea255c9e98477b47a56e03df4906e920eb2db57c28' ;; 		aarch64) arch='arm64';   sha256='f1c713711bf547185b82139bb4413b0409a6849be918dc29ea08ec04a6f72806' ;; 		armhf)   arch='armv6';   sha256='364d4da480737627849892e4656bccdda4370007fac655b02e0c3cebe87e14a6' ;; 		armv7)   arch='armv7';   sha256='e989455bd142736873fbd77ea6e574a079958644527d8716e381fc6545a91a8a' ;; 		ppc64le) arch='ppc64le'; sha256='377f0f56d4a9eab32630856a6357b245d89050137e433b538c35aafc3b713580' ;; 		s390x)   arch='s390x';   sha256='66f63e84d7adf02d0b7d8a821c618c464970de3d1726dd1a13c2149a71798f53' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:48 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:48 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:49 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:49 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376ba25ac41cec041d831e456ad293ec2efd7e4fd1357ae113210bfddd447a5f`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 286.7 KB (286653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd51371a508db5d3b5708d45eddb595bddc28f8c1a985b3eee93a4febcd14c4`  
		Last Modified: Wed, 10 May 2023 00:00:23 GMT  
		Size: 5.2 MB (5243839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c45c18e92d0b4cd85fc12dbf6086c1d26828468f3296c06f4fee43e339c5d2`  
		Last Modified: Wed, 10 May 2023 00:00:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17201b1df58c7847e6bd7b0a3afc3fa8a5fae78ae1e00fef66c8bbd7241f445e`  
		Last Modified: Wed, 10 May 2023 00:00:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.2-beta.2` - linux; s390x

```console
$ docker pull registry@sha256:df9f0496352ebb85973282e1d389bbc9e14aef42b257d2306479f8caa4dd832f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9163192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c34be771a16d266e03859c2be7e0d371e73bbf1198be3295e00594a90be47f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:53 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:01:01 GMT
RUN set -eux; 	version='2.8.2-beta.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f16957fe46a797439892bcea255c9e98477b47a56e03df4906e920eb2db57c28' ;; 		aarch64) arch='arm64';   sha256='f1c713711bf547185b82139bb4413b0409a6849be918dc29ea08ec04a6f72806' ;; 		armhf)   arch='armv6';   sha256='364d4da480737627849892e4656bccdda4370007fac655b02e0c3cebe87e14a6' ;; 		armv7)   arch='armv7';   sha256='e989455bd142736873fbd77ea6e574a079958644527d8716e381fc6545a91a8a' ;; 		ppc64le) arch='ppc64le'; sha256='377f0f56d4a9eab32630856a6357b245d89050137e433b538c35aafc3b713580' ;; 		s390x)   arch='s390x';   sha256='66f63e84d7adf02d0b7d8a821c618c464970de3d1726dd1a13c2149a71798f53' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:01:01 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:01:01 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:01:02 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:01:02 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:01:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:01:02 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72fc573296d33547281b8f37ff15a477a2844bdd1fff61bf191b5f18e14354`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 285.1 KB (285083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d0aaa8f867692f745ffbcd5a55164434440d820686d3286cd2dc081bb39024`  
		Last Modified: Wed, 10 May 2023 00:01:21 GMT  
		Size: 5.7 MB (5651194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128f2b5b382f9a88f7ef54f7a7a0cca9f5e4377c55b1df53a82bd7232b55e4f2`  
		Last Modified: Wed, 10 May 2023 00:01:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3072f8dc550d23c904f0cd50929980d1da40c8dfe1c3af9edd55ca948aa3a`  
		Last Modified: Wed, 10 May 2023 00:01:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:dbaa3e69f563fc146f3337eb9de422f74f6765bf0203c891ddfbd74a6f9b56eb
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
$ docker pull registry@sha256:85d4cd48754d4e8e4d4fe933bbde017d969e0e20775507add9faca39064bf9b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9788612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5352b75f67e2e2df2bf2d96509248d1f618b8aa66d8b8c89d21e29111424881`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:10 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:11 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:12 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:12 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:12 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:12 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58116d8bf56953e5f30b7f50257c5bb2b5ba4aba460cb69f2ac57eea00aaa5dc`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f7fac5d815c6d815af9cd4a55d79c15f938c8b4dfbec0699b4155800cba752`  
		Last Modified: Wed, 10 May 2023 00:00:25 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe88d67f473ca63bdce57cf03a3e2ed2e201809c472970040b018f538a841789`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a19664cea732d19655fe73f24b0b3c22ddf2b51bb3fbb005ba651fb1febbcf`  
		Last Modified: Wed, 10 May 2023 00:00:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:d002d4633b9d68ce336392e040ebd59a7ded522a3b479ed27068c7b1bc850601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9111855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff01fee827325890213929b64bc64d57bebe0e60798a5adb7745a95592c8165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:14 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:15 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:15 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:15 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:15 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a91154cf231582e0efd441a318760e357cccbcf664976f729d125fe63ccdc9`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 284.9 KB (284873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c865dcda756b3c78f5ed3ccb692d9e91d983a5bf4fa36351deff5fee6ec21ca1`  
		Last Modified: Tue, 09 May 2023 23:59:28 GMT  
		Size: 5.7 MB (5670689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40aa56ff6ea566e4022595c66d8d2f212fb790ccc5d167eddbb3d32e4b35ef71`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3e86673f0f8b7c433c179708f86adb1c4e3a774b7a03eeea9cc4844c3b5b46`  
		Last Modified: Tue, 09 May 2023 23:59:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:da7bd08bbb9ff20403dcc1ecea6671c592536494f042393d218da481292699de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8861467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e4ff48c67c5c89f42c3252d77bcc3a814f923527a0fcb530062a7ef77b07a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:07:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:07:22 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:07:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:07:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:07:22 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:07:23 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:07:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:07:23 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7807d1567ad70e9e42db0b7a4aa54ab9afc3df1c31c3fb590ced28192601e947`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 284.1 KB (284075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eb023c6817a3b9fc48c3958a6d1a0a77c801d2803b75aa39237bf63c9a4fab`  
		Last Modified: Wed, 10 May 2023 00:07:36 GMT  
		Size: 5.7 MB (5665662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c68a60bbd4090f3c9e80eded44a78e4d66ed9f4b5ec431bc24ecc695d3d45`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae7d509d894975670d3fb6419ae740f2ed1f394bb11fc386dcf9db9701c564b`  
		Last Modified: Wed, 10 May 2023 00:07:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:75182a34805c0e5b65b66c1a2702ca7392bf8e6319d7b638df3358fb60ee8a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9174198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e8344540f85b91a4c88972a2bd60223931511ef2bd5a4fbf65cd9149f0ec64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:03:32 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:03:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:03:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:03:34 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:03:34 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:03:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:03:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:03:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683203a1cdbff667eb41c5b6d8426e77bcb98ede7a1aaf8def0259eab83f01c`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 286.3 KB (286287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be85afcbc03b911e9fb6381ab096985863d6972399163ab7bc1bad5d744e415`  
		Last Modified: Wed, 10 May 2023 00:03:46 GMT  
		Size: 5.5 MB (5544450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d211ac8fe2c79895180de976eb58b670c6b2f8ff29193c51ce52d0d9f2a6b30`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb7494219ddef2a0aeb7e5f5c952ec1f17a029677789977c171067bc436bd5b`  
		Last Modified: Wed, 10 May 2023 00:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:606048bcc76d6ac565e5378e41b30d1447ab15e07cd05a617006f2c8745642ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8988190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04ec80703233aa9c104cc1dd3e85049bffc357feaafd0100fbf4e76ad5173e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Tue, 09 May 2023 23:59:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 09 May 2023 23:59:41 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 09 May 2023 23:59:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 09 May 2023 23:59:42 GMT
VOLUME [/var/lib/registry]
# Tue, 09 May 2023 23:59:42 GMT
EXPOSE 5000
# Tue, 09 May 2023 23:59:42 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 09 May 2023 23:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 May 2023 23:59:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376ba25ac41cec041d831e456ad293ec2efd7e4fd1357ae113210bfddd447a5f`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 286.7 KB (286653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21243f56c5e44c90b754e10c5b0101e1b0e71f3ce26255c2db38670818536cf`  
		Last Modified: Wed, 10 May 2023 00:00:01 GMT  
		Size: 5.3 MB (5315293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a5f39c1ca311071521e42d1025b4ade032b4bcbbeea140c62b46831bf83ce`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a628ae12d6f1c29427a7b657cda078084f20bc6d213b66e1836dd847d43875`  
		Last Modified: Wed, 10 May 2023 00:00:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:3643cb1566457855bce020926ab2cf0397dd36e107705583d0bb283846eccb13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9059cff0d5eb82a211218ca2620baa870c6a9512496c6a98031ea0a6556b055`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 00:00:53 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 May 2023 00:00:54 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 May 2023 00:00:55 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 May 2023 00:00:55 GMT
VOLUME [/var/lib/registry]
# Wed, 10 May 2023 00:00:55 GMT
EXPOSE 5000
# Wed, 10 May 2023 00:00:55 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 May 2023 00:00:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 00:00:55 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72fc573296d33547281b8f37ff15a477a2844bdd1fff61bf191b5f18e14354`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 285.1 KB (285083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e188748775a448f897c6a25bfdce905cb74d8b7b0c0a1899a867bd3677db2f`  
		Last Modified: Wed, 10 May 2023 00:01:13 GMT  
		Size: 5.8 MB (5811556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f887ef46f44c51c511fa48d46cdb0dfa53066f4aedc1790b598854cdeae91c2c`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26522c7f8863cd49e70bb220c4a24b383166089e129f7ce496feaf97100e317f`  
		Last Modified: Wed, 10 May 2023 00:01:12 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
