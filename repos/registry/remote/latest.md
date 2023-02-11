## `registry:latest`

```console
$ docker pull registry@sha256:f1f4dc1456165a8a30d5a6fb60191e1ea32a873b85b2e0ce1b59513b58208749
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
$ docker pull registry@sha256:cc6393207bf9d3e032c4d9277834c1695117532c9f7e8c64e7b7adcda3a85f39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c944c2288b6f3f01f348185f9b371223f2f5148df4f8331420efe34712b7ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:48:10 GMT
RUN apk add --no-cache ca-certificates
# Sat, 12 Nov 2022 10:00:43 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 12 Nov 2022 10:00:43 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 12 Nov 2022 10:00:44 GMT
VOLUME [/var/lib/registry]
# Sat, 12 Nov 2022 10:00:44 GMT
EXPOSE 5000
# Sat, 12 Nov 2022 10:00:44 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 12 Nov 2022 10:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Nov 2022 10:00:44 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41ae7ad2b39813485dabd88ae2e5ddce71b71a47d19af1377b0251055edf373`  
		Last Modified: Sat, 12 Nov 2022 10:00:55 GMT  
		Size: 284.7 KB (284748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0fc8a61618b72556b8786485226f9d7256c3449e2d9f5978d8dc4fc951319`  
		Last Modified: Sat, 12 Nov 2022 10:00:56 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21df229223d282438b1d9c577db207670dcdb6f392e923c57f91c66dcd3a753f`  
		Last Modified: Sat, 12 Nov 2022 10:00:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626897ccab21a4958a2934d04bae0c2df453a3e46ae144395cd0fc418ae757ac`  
		Last Modified: Sat, 12 Nov 2022 10:00:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:816cf44f043d0bc241c932b51be430353d3966224bbdfed376f31a3b3df8e9c5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8572680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc1398fe0186a534293d1fceb3ba9a11eb83d72d8be8150049261fcb50217ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:51:35 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 06:51:15 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 11 Feb 2023 06:51:15 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 11 Feb 2023 06:51:15 GMT
VOLUME [/var/lib/registry]
# Sat, 11 Feb 2023 06:51:15 GMT
EXPOSE 5000
# Sat, 11 Feb 2023 06:51:15 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 11 Feb 2023 06:51:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:51:16 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccaf948d29a6df6521083952d3dd3c3fa73f4d7ab10a9042ef096d8c1c3d0df`  
		Last Modified: Fri, 10 Feb 2023 22:00:52 GMT  
		Size: 284.6 KB (284632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803f0c5bb4acccc976d2828ba9f4b5c9c7f6a562ced28703b7dcdd0289817ab3`  
		Last Modified: Sat, 11 Feb 2023 06:51:35 GMT  
		Size: 5.7 MB (5670687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad74c93e0b112a31bb47b654d0eaa108dd0f66fd0f891ce3a5e4b757b3b2a628`  
		Last Modified: Sat, 11 Feb 2023 06:51:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986f27daf81e4691cbf44650de7712c2ad51c615aae77c162309b8bc726674a`  
		Last Modified: Sat, 11 Feb 2023 06:51:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:389b82bf4f1bbbf37f80dc583a9fc5832d47c21dc700a228b6fa1a1d8499a5a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8370528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcc2ddc633b8b2173f57308505363102c16a12d686027dcbc3a669d0c87edcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:37:15 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 05:59:19 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 11 Feb 2023 05:59:19 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 11 Feb 2023 05:59:19 GMT
VOLUME [/var/lib/registry]
# Sat, 11 Feb 2023 05:59:19 GMT
EXPOSE 5000
# Sat, 11 Feb 2023 05:59:20 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 11 Feb 2023 05:59:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:59:20 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b1795210cb30229a21e1859afbd6a84b3ce28287d75016e51da11886075f02`  
		Last Modified: Fri, 10 Feb 2023 23:50:59 GMT  
		Size: 283.8 KB (283787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bbf424b9fb95d83b6b69a3fb2f046289bb42966efdb6419b0fa03d54a3efb1`  
		Last Modified: Sat, 11 Feb 2023 05:59:41 GMT  
		Size: 5.7 MB (5665663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3fd1cf6616cbce6893ec0c914017a60ed52a49408b41bfd063db0932616c0d`  
		Last Modified: Sat, 11 Feb 2023 05:59:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39588d9ec8cd8407dbdda22a7d8deaf7497325573aad9da597bcc77594f377`  
		Last Modified: Sat, 11 Feb 2023 05:59:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:30bdc22b9f43c3fa2c1e955a07c28b7aa6af744339a24ca7af77a14d34a15a43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8539317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d8d61987f0b3ad20c87d463a29f5933aea84eaff3f7ae0ecfe8dc5c1d656e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:39:42 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 05:21:48 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 11 Feb 2023 05:21:49 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 11 Feb 2023 05:21:49 GMT
VOLUME [/var/lib/registry]
# Sat, 11 Feb 2023 05:21:49 GMT
EXPOSE 5000
# Sat, 11 Feb 2023 05:21:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 11 Feb 2023 05:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:21:49 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b230cb717c2f6d0b0d8da7bd0c2b11b9518f522267293c11e848e5dcd59ead18`  
		Last Modified: Fri, 10 Feb 2023 22:44:50 GMT  
		Size: 284.7 KB (284745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61411b6ba75de2abb623d7eede913dbbf73c5a6755bf0e4dc005699bcdec8ff7`  
		Last Modified: Sat, 11 Feb 2023 05:22:00 GMT  
		Size: 5.5 MB (5544455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc946fb4e36c99643c989f748d43ee976d2811eba351e22004df1eee9562a20`  
		Last Modified: Sat, 11 Feb 2023 05:21:59 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b093b20d22ac8aa0cef96e709c44586d9e911651eacecf9553989fead02071b`  
		Last Modified: Sat, 11 Feb 2023 05:21:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:5eafcf1bf7750996da3a9176389c3209e5fe81d1488bc4154abd67caa38272ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8404199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f68e3a6fb691a3784c0bd968fca7e89579b97c84a26f6de5e0c809c5b33b3be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:58:49 GMT
RUN apk add --no-cache ca-certificates
# Sat, 12 Nov 2022 11:44:15 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 12 Nov 2022 11:44:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 12 Nov 2022 11:44:16 GMT
VOLUME [/var/lib/registry]
# Sat, 12 Nov 2022 11:44:16 GMT
EXPOSE 5000
# Sat, 12 Nov 2022 11:44:17 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 12 Nov 2022 11:44:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Nov 2022 11:44:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64837ee1267e21bf6630225438d803884d3e2a45c80fd38b76ad1c92bf3f500f`  
		Last Modified: Sat, 12 Nov 2022 11:44:35 GMT  
		Size: 286.8 KB (286754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2fd18dd29331f9627d99a38b6e9a15e40943c9463d67fcc738e9348c86018d`  
		Last Modified: Sat, 12 Nov 2022 11:44:37 GMT  
		Size: 5.3 MB (5315281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c441324121ad43543c57d498f805616725062fadab9251faa9b43823a705ea81`  
		Last Modified: Sat, 12 Nov 2022 11:44:35 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04178ad9b3d83c279444f877ca6c9d1dec41c966d498e4ca8b803252f4932ae1`  
		Last Modified: Sat, 12 Nov 2022 11:44:35 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:bd1ba442e6a870849c99099164635ef2f835bde25ecb5026fe3b3b4472c50caf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8690723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6bcf462dfbb29ed6e8c011b7c5cba36ab50a290dd5efbdce215d984f5bd6d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:29:49 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 05:19:43 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 11 Feb 2023 05:19:43 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 11 Feb 2023 05:19:43 GMT
VOLUME [/var/lib/registry]
# Sat, 11 Feb 2023 05:19:44 GMT
EXPOSE 5000
# Sat, 11 Feb 2023 05:19:44 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 11 Feb 2023 05:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:19:44 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7d68246e7ba43f56a6b714e0428299028fcb1e6ccb9328a3b57e048cc3090b`  
		Last Modified: Fri, 10 Feb 2023 22:37:51 GMT  
		Size: 285.0 KB (284975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3361b15474a6fcc871a4fc2db168571ac2fc836a8af453f30266b59c71e80c87`  
		Last Modified: Sat, 11 Feb 2023 05:20:00 GMT  
		Size: 5.8 MB (5811555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803cdc38b87001d3b8eb8eb2b69a13d235c38096adbb75724f735e966ca96d0e`  
		Last Modified: Sat, 11 Feb 2023 05:19:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac5c55651fd0ee0713f16f5e8da199613526d2f71314d506a577b6bb4fbfe2`  
		Last Modified: Sat, 11 Feb 2023 05:19:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
