<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.1`](#registry281)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:dabe77465b261ccc0c4eca74968ae759b38c535a51841aa3145ed5bc97c31a2b
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
$ docker pull registry@sha256:5c98b00f91e8daed324cb680661e9d647f09d825778493ffb2618ff36bec2a9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3241e050fc981849fc396c054aa87da6b1e2d748ee46cd3e71bf89050881631`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:38:44 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 16:55:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 16:55:34 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 16:55:34 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 16:55:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 16:55:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b494d572400cf4b26beff6a89af57b70fbc1d7a2c1aa7a0d7b67c756bdaed61`  
		Last Modified: Tue, 29 Mar 2022 08:48:36 GMT  
		Size: 272.0 KB (271969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce0e919729180f43f37c386397ee7df6154e172f4f104c7196572d2eb88919`  
		Last Modified: Tue, 29 Mar 2022 16:55:47 GMT  
		Size: 6.1 MB (6105809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fec280ccc88586d94f581861ff02b7e9c16fc128e61be7315365e18efa9994f`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d637f99b74411f98a3d6a4e4f9a496eac649828eac5253d596eac97128af1aaf`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:a609eefdd40a571b0547b212d0211b024e0db6a4ce488395cdd6fbaf64069a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8565370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70d96992ad7722448dde4ff927afb31cabb3ca3625340d9bce09cc824c1cf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:40:30 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 08:26:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 08:26:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 08:26:13 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 08:26:13 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 08:26:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 08:26:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026b5f27b2698e668042c86dd2538d12d411867d83d2a9d9af230e055fe5a181`  
		Last Modified: Tue, 29 Mar 2022 07:57:23 GMT  
		Size: 272.1 KB (272137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602583abfce5deba8fd045228cf4ce4173d9ecfd600f2b196faa97e7155f4e60`  
		Last Modified: Tue, 29 Mar 2022 08:26:51 GMT  
		Size: 5.7 MB (5670678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222aa677428e4b0c08d63de3871514b0ad6c04a131110318fb97239e0f59f80`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5200b17ed8a4a315c67cbf064c2b662f9e1a5a4c654b340a1f2999984d24f665`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:93abd5c28b36fb71bd1ebc7eac93ffa6656e9d5133817fa0105d869084a42966
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8364443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcaf7118f1b5572c3cbc34dd5daaf9d1f01f0c9cdb3f07cb13bf2340bf77678e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 02:42:02 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 02:42:03 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 02:42:03 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 02:42:04 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 02:42:04 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 02:42:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac2eda75170d6732d6009c786b5360931d47a2b22d914b89a6aa610ea659ec`  
		Last Modified: Thu, 24 Mar 2022 02:42:41 GMT  
		Size: 5.7 MB (5665663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d109779e8f8fc44cc00f220b491fb3b4e7ad0ac287a8e7147a3a2012e92b3e0`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95639fad0218aecbb9a0ba384eea15cd0d591c1826ec5f056509b88f12002687`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:5120de3244ebbe2181b5b4f50199c7e1223b9040a8b9408a0dd6861af1709e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c776ad7009a101b19b19fc4bee357848c7ca9a23175b5d97c3a589f3ff606a25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 08:40:44 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 08:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 08:40:46 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 08:40:47 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 08:40:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 08:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 08:40:50 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7c1c2b0748ea98b6e11d552c14c4f86dae07d5667c478a03bd6eab4e1c8cdf`  
		Last Modified: Thu, 24 Mar 2022 08:41:09 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d7ec052b5ad746189fc9e794b4116bf51127f5683f29833fb45286883ff07`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372bb0b41175e4967a1376630854592f8c1c215cdc27d971cdf47b1697b16c1`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:ad1eda3a837566e2756f586e2773f6359ef2a5527715199ae0cb39e5e84ea9be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8404114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8d103b7166b2ec8259048deecf490f2dc8349c9ef11048540023b31e034f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 23:38:05 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 23:38:07 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 23:38:14 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 23:38:16 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 23:38:20 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 23:38:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 23:38:30 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7302f9407f2d1cff53ce1e0596fed540b7ae92dfbfc920f2cbd62c724b36f040`  
		Last Modified: Wed, 23 Mar 2022 23:38:58 GMT  
		Size: 5.3 MB (5315296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5011ba44e9b94bf90cdb9711dba341bb50c518ad328253639b1784b130eff4`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cfeb8ebc75a7104f66695bf68dfaea11389feab22461fa522bdd727a70032e`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:c9d065c51c74502411cbcac8ba65458aafbd09ed97300c0b3fba98ebfe7e05aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c8d181a700a502fbcb8b8892d993465d9a4cf50de5284e808541fa4c62ba27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 20:57:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 20:57:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 20:57:13 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 20:57:13 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 20:57:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 20:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 20:57:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cee07bc85ca77e787ec65fe17f9783075a16d756a4a9f0126f529572fae79b`  
		Last Modified: Wed, 23 Mar 2022 20:57:37 GMT  
		Size: 5.8 MB (5811548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b65b9d6a23d4e3830d24c55f24c1e8859c4af09aef34e06042266b37e09c0c`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a0ef686348864d3f290746b6724c627e4692544f247fc3c0a6157e5e49d74f`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8`

```console
$ docker pull registry@sha256:dabe77465b261ccc0c4eca74968ae759b38c535a51841aa3145ed5bc97c31a2b
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
$ docker pull registry@sha256:5c98b00f91e8daed324cb680661e9d647f09d825778493ffb2618ff36bec2a9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3241e050fc981849fc396c054aa87da6b1e2d748ee46cd3e71bf89050881631`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:38:44 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 16:55:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 16:55:34 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 16:55:34 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 16:55:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 16:55:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b494d572400cf4b26beff6a89af57b70fbc1d7a2c1aa7a0d7b67c756bdaed61`  
		Last Modified: Tue, 29 Mar 2022 08:48:36 GMT  
		Size: 272.0 KB (271969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce0e919729180f43f37c386397ee7df6154e172f4f104c7196572d2eb88919`  
		Last Modified: Tue, 29 Mar 2022 16:55:47 GMT  
		Size: 6.1 MB (6105809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fec280ccc88586d94f581861ff02b7e9c16fc128e61be7315365e18efa9994f`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d637f99b74411f98a3d6a4e4f9a496eac649828eac5253d596eac97128af1aaf`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:a609eefdd40a571b0547b212d0211b024e0db6a4ce488395cdd6fbaf64069a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8565370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70d96992ad7722448dde4ff927afb31cabb3ca3625340d9bce09cc824c1cf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:40:30 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 08:26:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 08:26:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 08:26:13 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 08:26:13 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 08:26:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 08:26:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026b5f27b2698e668042c86dd2538d12d411867d83d2a9d9af230e055fe5a181`  
		Last Modified: Tue, 29 Mar 2022 07:57:23 GMT  
		Size: 272.1 KB (272137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602583abfce5deba8fd045228cf4ce4173d9ecfd600f2b196faa97e7155f4e60`  
		Last Modified: Tue, 29 Mar 2022 08:26:51 GMT  
		Size: 5.7 MB (5670678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222aa677428e4b0c08d63de3871514b0ad6c04a131110318fb97239e0f59f80`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5200b17ed8a4a315c67cbf064c2b662f9e1a5a4c654b340a1f2999984d24f665`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:93abd5c28b36fb71bd1ebc7eac93ffa6656e9d5133817fa0105d869084a42966
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8364443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcaf7118f1b5572c3cbc34dd5daaf9d1f01f0c9cdb3f07cb13bf2340bf77678e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 02:42:02 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 02:42:03 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 02:42:03 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 02:42:04 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 02:42:04 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 02:42:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac2eda75170d6732d6009c786b5360931d47a2b22d914b89a6aa610ea659ec`  
		Last Modified: Thu, 24 Mar 2022 02:42:41 GMT  
		Size: 5.7 MB (5665663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d109779e8f8fc44cc00f220b491fb3b4e7ad0ac287a8e7147a3a2012e92b3e0`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95639fad0218aecbb9a0ba384eea15cd0d591c1826ec5f056509b88f12002687`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:5120de3244ebbe2181b5b4f50199c7e1223b9040a8b9408a0dd6861af1709e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c776ad7009a101b19b19fc4bee357848c7ca9a23175b5d97c3a589f3ff606a25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 08:40:44 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 08:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 08:40:46 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 08:40:47 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 08:40:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 08:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 08:40:50 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7c1c2b0748ea98b6e11d552c14c4f86dae07d5667c478a03bd6eab4e1c8cdf`  
		Last Modified: Thu, 24 Mar 2022 08:41:09 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d7ec052b5ad746189fc9e794b4116bf51127f5683f29833fb45286883ff07`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372bb0b41175e4967a1376630854592f8c1c215cdc27d971cdf47b1697b16c1`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:ad1eda3a837566e2756f586e2773f6359ef2a5527715199ae0cb39e5e84ea9be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8404114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8d103b7166b2ec8259048deecf490f2dc8349c9ef11048540023b31e034f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 23:38:05 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 23:38:07 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 23:38:14 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 23:38:16 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 23:38:20 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 23:38:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 23:38:30 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7302f9407f2d1cff53ce1e0596fed540b7ae92dfbfc920f2cbd62c724b36f040`  
		Last Modified: Wed, 23 Mar 2022 23:38:58 GMT  
		Size: 5.3 MB (5315296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5011ba44e9b94bf90cdb9711dba341bb50c518ad328253639b1784b130eff4`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cfeb8ebc75a7104f66695bf68dfaea11389feab22461fa522bdd727a70032e`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:c9d065c51c74502411cbcac8ba65458aafbd09ed97300c0b3fba98ebfe7e05aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c8d181a700a502fbcb8b8892d993465d9a4cf50de5284e808541fa4c62ba27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 20:57:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 20:57:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 20:57:13 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 20:57:13 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 20:57:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 20:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 20:57:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cee07bc85ca77e787ec65fe17f9783075a16d756a4a9f0126f529572fae79b`  
		Last Modified: Wed, 23 Mar 2022 20:57:37 GMT  
		Size: 5.8 MB (5811548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b65b9d6a23d4e3830d24c55f24c1e8859c4af09aef34e06042266b37e09c0c`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a0ef686348864d3f290746b6724c627e4692544f247fc3c0a6157e5e49d74f`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8.1`

```console
$ docker pull registry@sha256:dabe77465b261ccc0c4eca74968ae759b38c535a51841aa3145ed5bc97c31a2b
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
$ docker pull registry@sha256:5c98b00f91e8daed324cb680661e9d647f09d825778493ffb2618ff36bec2a9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3241e050fc981849fc396c054aa87da6b1e2d748ee46cd3e71bf89050881631`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:38:44 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 16:55:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 16:55:34 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 16:55:34 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 16:55:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 16:55:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b494d572400cf4b26beff6a89af57b70fbc1d7a2c1aa7a0d7b67c756bdaed61`  
		Last Modified: Tue, 29 Mar 2022 08:48:36 GMT  
		Size: 272.0 KB (271969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce0e919729180f43f37c386397ee7df6154e172f4f104c7196572d2eb88919`  
		Last Modified: Tue, 29 Mar 2022 16:55:47 GMT  
		Size: 6.1 MB (6105809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fec280ccc88586d94f581861ff02b7e9c16fc128e61be7315365e18efa9994f`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d637f99b74411f98a3d6a4e4f9a496eac649828eac5253d596eac97128af1aaf`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:a609eefdd40a571b0547b212d0211b024e0db6a4ce488395cdd6fbaf64069a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8565370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70d96992ad7722448dde4ff927afb31cabb3ca3625340d9bce09cc824c1cf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:40:30 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 08:26:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 08:26:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 08:26:13 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 08:26:13 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 08:26:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 08:26:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026b5f27b2698e668042c86dd2538d12d411867d83d2a9d9af230e055fe5a181`  
		Last Modified: Tue, 29 Mar 2022 07:57:23 GMT  
		Size: 272.1 KB (272137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602583abfce5deba8fd045228cf4ce4173d9ecfd600f2b196faa97e7155f4e60`  
		Last Modified: Tue, 29 Mar 2022 08:26:51 GMT  
		Size: 5.7 MB (5670678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222aa677428e4b0c08d63de3871514b0ad6c04a131110318fb97239e0f59f80`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5200b17ed8a4a315c67cbf064c2b662f9e1a5a4c654b340a1f2999984d24f665`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:93abd5c28b36fb71bd1ebc7eac93ffa6656e9d5133817fa0105d869084a42966
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8364443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcaf7118f1b5572c3cbc34dd5daaf9d1f01f0c9cdb3f07cb13bf2340bf77678e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 02:42:02 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 02:42:03 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 02:42:03 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 02:42:04 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 02:42:04 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 02:42:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac2eda75170d6732d6009c786b5360931d47a2b22d914b89a6aa610ea659ec`  
		Last Modified: Thu, 24 Mar 2022 02:42:41 GMT  
		Size: 5.7 MB (5665663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d109779e8f8fc44cc00f220b491fb3b4e7ad0ac287a8e7147a3a2012e92b3e0`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95639fad0218aecbb9a0ba384eea15cd0d591c1826ec5f056509b88f12002687`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:5120de3244ebbe2181b5b4f50199c7e1223b9040a8b9408a0dd6861af1709e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c776ad7009a101b19b19fc4bee357848c7ca9a23175b5d97c3a589f3ff606a25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 08:40:44 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 08:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 08:40:46 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 08:40:47 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 08:40:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 08:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 08:40:50 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7c1c2b0748ea98b6e11d552c14c4f86dae07d5667c478a03bd6eab4e1c8cdf`  
		Last Modified: Thu, 24 Mar 2022 08:41:09 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d7ec052b5ad746189fc9e794b4116bf51127f5683f29833fb45286883ff07`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372bb0b41175e4967a1376630854592f8c1c215cdc27d971cdf47b1697b16c1`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; ppc64le

```console
$ docker pull registry@sha256:ad1eda3a837566e2756f586e2773f6359ef2a5527715199ae0cb39e5e84ea9be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8404114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8d103b7166b2ec8259048deecf490f2dc8349c9ef11048540023b31e034f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 23:38:05 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 23:38:07 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 23:38:14 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 23:38:16 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 23:38:20 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 23:38:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 23:38:30 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7302f9407f2d1cff53ce1e0596fed540b7ae92dfbfc920f2cbd62c724b36f040`  
		Last Modified: Wed, 23 Mar 2022 23:38:58 GMT  
		Size: 5.3 MB (5315296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5011ba44e9b94bf90cdb9711dba341bb50c518ad328253639b1784b130eff4`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cfeb8ebc75a7104f66695bf68dfaea11389feab22461fa522bdd727a70032e`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; s390x

```console
$ docker pull registry@sha256:c9d065c51c74502411cbcac8ba65458aafbd09ed97300c0b3fba98ebfe7e05aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c8d181a700a502fbcb8b8892d993465d9a4cf50de5284e808541fa4c62ba27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 20:57:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 20:57:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 20:57:13 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 20:57:13 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 20:57:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 20:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 20:57:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cee07bc85ca77e787ec65fe17f9783075a16d756a4a9f0126f529572fae79b`  
		Last Modified: Wed, 23 Mar 2022 20:57:37 GMT  
		Size: 5.8 MB (5811548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b65b9d6a23d4e3830d24c55f24c1e8859c4af09aef34e06042266b37e09c0c`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a0ef686348864d3f290746b6724c627e4692544f247fc3c0a6157e5e49d74f`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:dabe77465b261ccc0c4eca74968ae759b38c535a51841aa3145ed5bc97c31a2b
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
$ docker pull registry@sha256:5c98b00f91e8daed324cb680661e9d647f09d825778493ffb2618ff36bec2a9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9192902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3241e050fc981849fc396c054aa87da6b1e2d748ee46cd3e71bf89050881631`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:38:44 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 16:55:34 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 16:55:34 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 16:55:34 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 16:55:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 16:55:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 16:55:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b494d572400cf4b26beff6a89af57b70fbc1d7a2c1aa7a0d7b67c756bdaed61`  
		Last Modified: Tue, 29 Mar 2022 08:48:36 GMT  
		Size: 272.0 KB (271969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce0e919729180f43f37c386397ee7df6154e172f4f104c7196572d2eb88919`  
		Last Modified: Tue, 29 Mar 2022 16:55:47 GMT  
		Size: 6.1 MB (6105809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fec280ccc88586d94f581861ff02b7e9c16fc128e61be7315365e18efa9994f`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d637f99b74411f98a3d6a4e4f9a496eac649828eac5253d596eac97128af1aaf`  
		Last Modified: Tue, 29 Mar 2022 16:55:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:a609eefdd40a571b0547b212d0211b024e0db6a4ce488395cdd6fbaf64069a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8565370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70d96992ad7722448dde4ff927afb31cabb3ca3625340d9bce09cc824c1cf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:40:30 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 08:26:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 29 Mar 2022 08:26:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 29 Mar 2022 08:26:13 GMT
VOLUME [/var/lib/registry]
# Tue, 29 Mar 2022 08:26:13 GMT
EXPOSE 5000
# Tue, 29 Mar 2022 08:26:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 29 Mar 2022 08:26:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026b5f27b2698e668042c86dd2538d12d411867d83d2a9d9af230e055fe5a181`  
		Last Modified: Tue, 29 Mar 2022 07:57:23 GMT  
		Size: 272.1 KB (272137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602583abfce5deba8fd045228cf4ce4173d9ecfd600f2b196faa97e7155f4e60`  
		Last Modified: Tue, 29 Mar 2022 08:26:51 GMT  
		Size: 5.7 MB (5670678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222aa677428e4b0c08d63de3871514b0ad6c04a131110318fb97239e0f59f80`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5200b17ed8a4a315c67cbf064c2b662f9e1a5a4c654b340a1f2999984d24f665`  
		Last Modified: Tue, 29 Mar 2022 08:26:48 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:93abd5c28b36fb71bd1ebc7eac93ffa6656e9d5133817fa0105d869084a42966
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8364443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcaf7118f1b5572c3cbc34dd5daaf9d1f01f0c9cdb3f07cb13bf2340bf77678e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 02:42:02 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 02:42:03 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 02:42:03 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 02:42:04 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 02:42:04 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 02:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 02:42:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac2eda75170d6732d6009c786b5360931d47a2b22d914b89a6aa610ea659ec`  
		Last Modified: Thu, 24 Mar 2022 02:42:41 GMT  
		Size: 5.7 MB (5665663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d109779e8f8fc44cc00f220b491fb3b4e7ad0ac287a8e7147a3a2012e92b3e0`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95639fad0218aecbb9a0ba384eea15cd0d591c1826ec5f056509b88f12002687`  
		Last Modified: Thu, 24 Mar 2022 02:42:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:5120de3244ebbe2181b5b4f50199c7e1223b9040a8b9408a0dd6861af1709e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c776ad7009a101b19b19fc4bee357848c7ca9a23175b5d97c3a589f3ff606a25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 08:40:44 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 24 Mar 2022 08:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 24 Mar 2022 08:40:46 GMT
VOLUME [/var/lib/registry]
# Thu, 24 Mar 2022 08:40:47 GMT
EXPOSE 5000
# Thu, 24 Mar 2022 08:40:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 24 Mar 2022 08:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 08:40:50 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7c1c2b0748ea98b6e11d552c14c4f86dae07d5667c478a03bd6eab4e1c8cdf`  
		Last Modified: Thu, 24 Mar 2022 08:41:09 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d7ec052b5ad746189fc9e794b4116bf51127f5683f29833fb45286883ff07`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372bb0b41175e4967a1376630854592f8c1c215cdc27d971cdf47b1697b16c1`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:ad1eda3a837566e2756f586e2773f6359ef2a5527715199ae0cb39e5e84ea9be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8404114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8d103b7166b2ec8259048deecf490f2dc8349c9ef11048540023b31e034f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 23:38:05 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 23:38:07 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 23:38:14 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 23:38:16 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 23:38:20 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 23:38:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 23:38:30 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7302f9407f2d1cff53ce1e0596fed540b7ae92dfbfc920f2cbd62c724b36f040`  
		Last Modified: Wed, 23 Mar 2022 23:38:58 GMT  
		Size: 5.3 MB (5315296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5011ba44e9b94bf90cdb9711dba341bb50c518ad328253639b1784b130eff4`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cfeb8ebc75a7104f66695bf68dfaea11389feab22461fa522bdd727a70032e`  
		Last Modified: Wed, 23 Mar 2022 23:38:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:c9d065c51c74502411cbcac8ba65458aafbd09ed97300c0b3fba98ebfe7e05aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c8d181a700a502fbcb8b8892d993465d9a4cf50de5284e808541fa4c62ba27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 20:57:12 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 23 Mar 2022 20:57:12 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 23 Mar 2022 20:57:13 GMT
VOLUME [/var/lib/registry]
# Wed, 23 Mar 2022 20:57:13 GMT
EXPOSE 5000
# Wed, 23 Mar 2022 20:57:14 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 23 Mar 2022 20:57:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Mar 2022 20:57:15 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cee07bc85ca77e787ec65fe17f9783075a16d756a4a9f0126f529572fae79b`  
		Last Modified: Wed, 23 Mar 2022 20:57:37 GMT  
		Size: 5.8 MB (5811548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b65b9d6a23d4e3830d24c55f24c1e8859c4af09aef34e06042266b37e09c0c`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a0ef686348864d3f290746b6724c627e4692544f247fc3c0a6157e5e49d74f`  
		Last Modified: Wed, 23 Mar 2022 20:57:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
