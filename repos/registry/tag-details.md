<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.1`](#registry281)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:1ebc37a5d075776378dc362bbfb7ecf5f67cba695f5833c5c9fe4be42c7f5632
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
$ docker pull registry@sha256:29f25d3b41a11500cc8fc4e19206d483833a68543c30aefc8c145c8b1f0b1450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0f7b0a13ef62e85d770396e1868bf919f4747743ece4f233895a246c436394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:16 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 01:21:49 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 01:21:49 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 01:21:49 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 01:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 01:21:49 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5299e6f7860564fd4df7e9a224f3d05dc26d0e855fb26ac7e9d9e156cf1422b2`  
		Last Modified: Tue, 09 Aug 2022 19:19:30 GMT  
		Size: 284.7 KB (284725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2fb79b7ce6b0abd6f8448fe016019030edc289f97327fe37b8dba13a5ef16a`  
		Last Modified: Wed, 10 Aug 2022 01:22:02 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a97d2d84d94d10a270600330cb860dbdf068ba87de665aadd18f8e3535edea`  
		Last Modified: Wed, 10 Aug 2022 01:22:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c4c74a95e4772391d5c7a2016dd41623a306d27e25b7060be844fb9f4ee0e2`  
		Last Modified: Wed, 10 Aug 2022 01:22:01 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:c9193715ce031a4adacdc422577ed7d59bea06f261db5efa06148ada1e2622c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8569920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c888cfa4e2c0407f52481fb95e993322a6b8be9f4e93837e0852f771a40748f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:55:06 GMT
RUN apk add --no-cache ca-certificates
# Thu, 11 Aug 2022 00:00:28 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 11 Aug 2022 00:00:28 GMT
VOLUME [/var/lib/registry]
# Thu, 11 Aug 2022 00:00:28 GMT
EXPOSE 5000
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 11 Aug 2022 00:00:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Aug 2022 00:00:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9c949f49fc8f526d6efc5da6670075476f51650be8b4471ba9b4b6e23b2ba`  
		Last Modified: Tue, 09 Aug 2022 19:19:26 GMT  
		Size: 284.7 KB (284675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c71446b2c03b8e2bc94167d3d3ec2a313dc829a959bb85d0daabd307248ba6`  
		Last Modified: Thu, 11 Aug 2022 00:00:48 GMT  
		Size: 5.7 MB (5670668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904c374b6acf45ffc25b5b1eba700fef9e2891ade700d450b86973aa5f4fd7d`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b946dba60cb877d6d42d9ce969d9c14f7223f5c5b527a019d5f333e7e862da6`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:ad71f9315971b16106ad17df051520c0f32a2cfe8aa4aff257890a2dd88276d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8349558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f8e344076df43f3a4c364f38d787f90a79c6b4c969c84524f16574642cfc4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:04:00 GMT
RUN apk add --no-cache ca-certificates
# Tue, 19 Jul 2022 09:40:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 19 Jul 2022 09:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 19 Jul 2022 09:40:46 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Jul 2022 09:40:47 GMT
EXPOSE 5000
# Tue, 19 Jul 2022 09:40:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 19 Jul 2022 09:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 09:40:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f310150171570b715e2477d77efca60a48d1ddbc81587d89c7cbc2460c1ed361`  
		Last Modified: Mon, 18 Jul 2022 23:20:36 GMT  
		Size: 271.0 KB (270981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19f7609aebfc923d4c2b6d8167f2f830f9da00342ae8b849e1d20ffb195e662`  
		Last Modified: Tue, 19 Jul 2022 09:41:23 GMT  
		Size: 5.7 MB (5665659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a97de6c3e438f862a84820088419b83e84dfb6eda271bdfc6ddbd53c9d5b395`  
		Last Modified: Tue, 19 Jul 2022 09:41:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bd26b7e8bcd288a5dc04cb590110031fdc4216521991ee38323a219ac84ab6`  
		Last Modified: Tue, 19 Jul 2022 09:41:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:561ecbab74a78b52e52585ced90a46293b0923ad1faa380b73ab2335aee444c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8537219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4206ae70dd03980535dcc9ba7f04c973396cc8b4f324d44a1e706180b8ec068c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:07:56 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 05:40:20 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 05:40:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 05:40:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 05:40:23 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 05:40:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 05:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 05:40:26 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817a8a8f634c3a78b1a3b55a03335868971f2378932d3454ece4e3bfc5931675`  
		Last Modified: Tue, 09 Aug 2022 19:16:28 GMT  
		Size: 284.5 KB (284523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e865e4194320147cb54c543dfd5bd97d2121560564e3462ac4b8e96c4e6b5a`  
		Last Modified: Wed, 10 Aug 2022 05:40:45 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2cbf89aa09d2c7ecfb5662a97fa7836400a28119c987154fae927f41dde54`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0dc4e47315c6766f7a9f98a9020dc73cb7bc469272cb700be6d438a4ed8e93`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:cc614c0da21cc46156655f767c1a99e8b9800135264736656d703f52acfa224b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8405964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355730cc5c16bb6422a7a4a9ae52935376e9a8de13adc44ba80ae79cf3d6edcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:01 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 02:18:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 02:18:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 02:18:24 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 02:18:24 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 02:18:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 02:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 02:18:25 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0369baf68c186e68d7c3cee256f5bc3a9351c6763ed88a03033834a5b942b700`  
		Last Modified: Tue, 09 Aug 2022 18:28:37 GMT  
		Size: 286.7 KB (286735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7899360365a91bf0dd803f7acfaba387f7f22011540b3d7686c96297666691f`  
		Last Modified: Wed, 10 Aug 2022 02:18:52 GMT  
		Size: 5.3 MB (5315294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7de731985617224f1bb2bc4be21f0443ccd1e9a0a2158cc4b227eeff291c2`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c665d99f8bec99576eb2116041d02399e02c1a6cf4975061f3c07b11c5c3eb`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:12dce2d9bb3e725aa26281fd87cc175ce59ba5e838be21d4cb55d4dc1ce6347c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8687708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08713d331991e2b249b6538e92397edaa76a6dab591b20d5ffa87cdedf241844`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:45:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 06:06:51 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 06:06:52 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 06:06:52 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 06:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 06:06:52 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3e6b82e3d7aa395eb79202f28debe691c40472030a94ade061f395a44b1cfa`  
		Last Modified: Tue, 09 Aug 2022 18:55:04 GMT  
		Size: 284.9 KB (284946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042f30c5c9587a452cc286399cf6e33745ec1f847cb3d89d0d0853be8822559`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 5.8 MB (5811552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ff5faf84b39cd18d6d132da5b7f47ba503c19e93f7933a74dc77e6be802c90`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bbd7b4221680f3dc40fe532e93e45f093a469cb030e5edb7cec6c84e75cfc8`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8`

```console
$ docker pull registry@sha256:1ebc37a5d075776378dc362bbfb7ecf5f67cba695f5833c5c9fe4be42c7f5632
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
$ docker pull registry@sha256:29f25d3b41a11500cc8fc4e19206d483833a68543c30aefc8c145c8b1f0b1450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0f7b0a13ef62e85d770396e1868bf919f4747743ece4f233895a246c436394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:16 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 01:21:49 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 01:21:49 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 01:21:49 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 01:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 01:21:49 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5299e6f7860564fd4df7e9a224f3d05dc26d0e855fb26ac7e9d9e156cf1422b2`  
		Last Modified: Tue, 09 Aug 2022 19:19:30 GMT  
		Size: 284.7 KB (284725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2fb79b7ce6b0abd6f8448fe016019030edc289f97327fe37b8dba13a5ef16a`  
		Last Modified: Wed, 10 Aug 2022 01:22:02 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a97d2d84d94d10a270600330cb860dbdf068ba87de665aadd18f8e3535edea`  
		Last Modified: Wed, 10 Aug 2022 01:22:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c4c74a95e4772391d5c7a2016dd41623a306d27e25b7060be844fb9f4ee0e2`  
		Last Modified: Wed, 10 Aug 2022 01:22:01 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:c9193715ce031a4adacdc422577ed7d59bea06f261db5efa06148ada1e2622c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8569920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c888cfa4e2c0407f52481fb95e993322a6b8be9f4e93837e0852f771a40748f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:55:06 GMT
RUN apk add --no-cache ca-certificates
# Thu, 11 Aug 2022 00:00:28 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 11 Aug 2022 00:00:28 GMT
VOLUME [/var/lib/registry]
# Thu, 11 Aug 2022 00:00:28 GMT
EXPOSE 5000
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 11 Aug 2022 00:00:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Aug 2022 00:00:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9c949f49fc8f526d6efc5da6670075476f51650be8b4471ba9b4b6e23b2ba`  
		Last Modified: Tue, 09 Aug 2022 19:19:26 GMT  
		Size: 284.7 KB (284675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c71446b2c03b8e2bc94167d3d3ec2a313dc829a959bb85d0daabd307248ba6`  
		Last Modified: Thu, 11 Aug 2022 00:00:48 GMT  
		Size: 5.7 MB (5670668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904c374b6acf45ffc25b5b1eba700fef9e2891ade700d450b86973aa5f4fd7d`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b946dba60cb877d6d42d9ce969d9c14f7223f5c5b527a019d5f333e7e862da6`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:ad71f9315971b16106ad17df051520c0f32a2cfe8aa4aff257890a2dd88276d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8349558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f8e344076df43f3a4c364f38d787f90a79c6b4c969c84524f16574642cfc4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:04:00 GMT
RUN apk add --no-cache ca-certificates
# Tue, 19 Jul 2022 09:40:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 19 Jul 2022 09:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 19 Jul 2022 09:40:46 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Jul 2022 09:40:47 GMT
EXPOSE 5000
# Tue, 19 Jul 2022 09:40:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 19 Jul 2022 09:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 09:40:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f310150171570b715e2477d77efca60a48d1ddbc81587d89c7cbc2460c1ed361`  
		Last Modified: Mon, 18 Jul 2022 23:20:36 GMT  
		Size: 271.0 KB (270981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19f7609aebfc923d4c2b6d8167f2f830f9da00342ae8b849e1d20ffb195e662`  
		Last Modified: Tue, 19 Jul 2022 09:41:23 GMT  
		Size: 5.7 MB (5665659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a97de6c3e438f862a84820088419b83e84dfb6eda271bdfc6ddbd53c9d5b395`  
		Last Modified: Tue, 19 Jul 2022 09:41:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bd26b7e8bcd288a5dc04cb590110031fdc4216521991ee38323a219ac84ab6`  
		Last Modified: Tue, 19 Jul 2022 09:41:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:561ecbab74a78b52e52585ced90a46293b0923ad1faa380b73ab2335aee444c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8537219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4206ae70dd03980535dcc9ba7f04c973396cc8b4f324d44a1e706180b8ec068c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:07:56 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 05:40:20 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 05:40:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 05:40:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 05:40:23 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 05:40:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 05:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 05:40:26 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817a8a8f634c3a78b1a3b55a03335868971f2378932d3454ece4e3bfc5931675`  
		Last Modified: Tue, 09 Aug 2022 19:16:28 GMT  
		Size: 284.5 KB (284523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e865e4194320147cb54c543dfd5bd97d2121560564e3462ac4b8e96c4e6b5a`  
		Last Modified: Wed, 10 Aug 2022 05:40:45 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2cbf89aa09d2c7ecfb5662a97fa7836400a28119c987154fae927f41dde54`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0dc4e47315c6766f7a9f98a9020dc73cb7bc469272cb700be6d438a4ed8e93`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:cc614c0da21cc46156655f767c1a99e8b9800135264736656d703f52acfa224b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8405964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355730cc5c16bb6422a7a4a9ae52935376e9a8de13adc44ba80ae79cf3d6edcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:01 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 02:18:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 02:18:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 02:18:24 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 02:18:24 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 02:18:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 02:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 02:18:25 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0369baf68c186e68d7c3cee256f5bc3a9351c6763ed88a03033834a5b942b700`  
		Last Modified: Tue, 09 Aug 2022 18:28:37 GMT  
		Size: 286.7 KB (286735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7899360365a91bf0dd803f7acfaba387f7f22011540b3d7686c96297666691f`  
		Last Modified: Wed, 10 Aug 2022 02:18:52 GMT  
		Size: 5.3 MB (5315294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7de731985617224f1bb2bc4be21f0443ccd1e9a0a2158cc4b227eeff291c2`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c665d99f8bec99576eb2116041d02399e02c1a6cf4975061f3c07b11c5c3eb`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:12dce2d9bb3e725aa26281fd87cc175ce59ba5e838be21d4cb55d4dc1ce6347c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8687708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08713d331991e2b249b6538e92397edaa76a6dab591b20d5ffa87cdedf241844`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:45:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 06:06:51 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 06:06:52 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 06:06:52 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 06:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 06:06:52 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3e6b82e3d7aa395eb79202f28debe691c40472030a94ade061f395a44b1cfa`  
		Last Modified: Tue, 09 Aug 2022 18:55:04 GMT  
		Size: 284.9 KB (284946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042f30c5c9587a452cc286399cf6e33745ec1f847cb3d89d0d0853be8822559`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 5.8 MB (5811552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ff5faf84b39cd18d6d132da5b7f47ba503c19e93f7933a74dc77e6be802c90`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bbd7b4221680f3dc40fe532e93e45f093a469cb030e5edb7cec6c84e75cfc8`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8.1`

```console
$ docker pull registry@sha256:1ebc37a5d075776378dc362bbfb7ecf5f67cba695f5833c5c9fe4be42c7f5632
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
$ docker pull registry@sha256:29f25d3b41a11500cc8fc4e19206d483833a68543c30aefc8c145c8b1f0b1450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0f7b0a13ef62e85d770396e1868bf919f4747743ece4f233895a246c436394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:16 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 01:21:49 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 01:21:49 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 01:21:49 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 01:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 01:21:49 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5299e6f7860564fd4df7e9a224f3d05dc26d0e855fb26ac7e9d9e156cf1422b2`  
		Last Modified: Tue, 09 Aug 2022 19:19:30 GMT  
		Size: 284.7 KB (284725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2fb79b7ce6b0abd6f8448fe016019030edc289f97327fe37b8dba13a5ef16a`  
		Last Modified: Wed, 10 Aug 2022 01:22:02 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a97d2d84d94d10a270600330cb860dbdf068ba87de665aadd18f8e3535edea`  
		Last Modified: Wed, 10 Aug 2022 01:22:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c4c74a95e4772391d5c7a2016dd41623a306d27e25b7060be844fb9f4ee0e2`  
		Last Modified: Wed, 10 Aug 2022 01:22:01 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:c9193715ce031a4adacdc422577ed7d59bea06f261db5efa06148ada1e2622c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8569920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c888cfa4e2c0407f52481fb95e993322a6b8be9f4e93837e0852f771a40748f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:55:06 GMT
RUN apk add --no-cache ca-certificates
# Thu, 11 Aug 2022 00:00:28 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 11 Aug 2022 00:00:28 GMT
VOLUME [/var/lib/registry]
# Thu, 11 Aug 2022 00:00:28 GMT
EXPOSE 5000
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 11 Aug 2022 00:00:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Aug 2022 00:00:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9c949f49fc8f526d6efc5da6670075476f51650be8b4471ba9b4b6e23b2ba`  
		Last Modified: Tue, 09 Aug 2022 19:19:26 GMT  
		Size: 284.7 KB (284675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c71446b2c03b8e2bc94167d3d3ec2a313dc829a959bb85d0daabd307248ba6`  
		Last Modified: Thu, 11 Aug 2022 00:00:48 GMT  
		Size: 5.7 MB (5670668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904c374b6acf45ffc25b5b1eba700fef9e2891ade700d450b86973aa5f4fd7d`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b946dba60cb877d6d42d9ce969d9c14f7223f5c5b527a019d5f333e7e862da6`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:ad71f9315971b16106ad17df051520c0f32a2cfe8aa4aff257890a2dd88276d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8349558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f8e344076df43f3a4c364f38d787f90a79c6b4c969c84524f16574642cfc4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:04:00 GMT
RUN apk add --no-cache ca-certificates
# Tue, 19 Jul 2022 09:40:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 19 Jul 2022 09:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 19 Jul 2022 09:40:46 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Jul 2022 09:40:47 GMT
EXPOSE 5000
# Tue, 19 Jul 2022 09:40:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 19 Jul 2022 09:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 09:40:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f310150171570b715e2477d77efca60a48d1ddbc81587d89c7cbc2460c1ed361`  
		Last Modified: Mon, 18 Jul 2022 23:20:36 GMT  
		Size: 271.0 KB (270981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19f7609aebfc923d4c2b6d8167f2f830f9da00342ae8b849e1d20ffb195e662`  
		Last Modified: Tue, 19 Jul 2022 09:41:23 GMT  
		Size: 5.7 MB (5665659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a97de6c3e438f862a84820088419b83e84dfb6eda271bdfc6ddbd53c9d5b395`  
		Last Modified: Tue, 19 Jul 2022 09:41:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bd26b7e8bcd288a5dc04cb590110031fdc4216521991ee38323a219ac84ab6`  
		Last Modified: Tue, 19 Jul 2022 09:41:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:561ecbab74a78b52e52585ced90a46293b0923ad1faa380b73ab2335aee444c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8537219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4206ae70dd03980535dcc9ba7f04c973396cc8b4f324d44a1e706180b8ec068c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:07:56 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 05:40:20 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 05:40:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 05:40:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 05:40:23 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 05:40:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 05:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 05:40:26 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817a8a8f634c3a78b1a3b55a03335868971f2378932d3454ece4e3bfc5931675`  
		Last Modified: Tue, 09 Aug 2022 19:16:28 GMT  
		Size: 284.5 KB (284523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e865e4194320147cb54c543dfd5bd97d2121560564e3462ac4b8e96c4e6b5a`  
		Last Modified: Wed, 10 Aug 2022 05:40:45 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2cbf89aa09d2c7ecfb5662a97fa7836400a28119c987154fae927f41dde54`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0dc4e47315c6766f7a9f98a9020dc73cb7bc469272cb700be6d438a4ed8e93`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; ppc64le

```console
$ docker pull registry@sha256:cc614c0da21cc46156655f767c1a99e8b9800135264736656d703f52acfa224b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8405964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355730cc5c16bb6422a7a4a9ae52935376e9a8de13adc44ba80ae79cf3d6edcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:01 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 02:18:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 02:18:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 02:18:24 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 02:18:24 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 02:18:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 02:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 02:18:25 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0369baf68c186e68d7c3cee256f5bc3a9351c6763ed88a03033834a5b942b700`  
		Last Modified: Tue, 09 Aug 2022 18:28:37 GMT  
		Size: 286.7 KB (286735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7899360365a91bf0dd803f7acfaba387f7f22011540b3d7686c96297666691f`  
		Last Modified: Wed, 10 Aug 2022 02:18:52 GMT  
		Size: 5.3 MB (5315294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7de731985617224f1bb2bc4be21f0443ccd1e9a0a2158cc4b227eeff291c2`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c665d99f8bec99576eb2116041d02399e02c1a6cf4975061f3c07b11c5c3eb`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.1` - linux; s390x

```console
$ docker pull registry@sha256:12dce2d9bb3e725aa26281fd87cc175ce59ba5e838be21d4cb55d4dc1ce6347c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8687708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08713d331991e2b249b6538e92397edaa76a6dab591b20d5ffa87cdedf241844`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:45:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 06:06:51 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 06:06:52 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 06:06:52 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 06:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 06:06:52 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3e6b82e3d7aa395eb79202f28debe691c40472030a94ade061f395a44b1cfa`  
		Last Modified: Tue, 09 Aug 2022 18:55:04 GMT  
		Size: 284.9 KB (284946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042f30c5c9587a452cc286399cf6e33745ec1f847cb3d89d0d0853be8822559`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 5.8 MB (5811552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ff5faf84b39cd18d6d132da5b7f47ba503c19e93f7933a74dc77e6be802c90`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bbd7b4221680f3dc40fe532e93e45f093a469cb030e5edb7cec6c84e75cfc8`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:1ebc37a5d075776378dc362bbfb7ecf5f67cba695f5833c5c9fe4be42c7f5632
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
$ docker pull registry@sha256:29f25d3b41a11500cc8fc4e19206d483833a68543c30aefc8c145c8b1f0b1450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0f7b0a13ef62e85d770396e1868bf919f4747743ece4f233895a246c436394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:16 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 01:21:49 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 01:21:49 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 01:21:49 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 01:21:49 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 01:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 01:21:49 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5299e6f7860564fd4df7e9a224f3d05dc26d0e855fb26ac7e9d9e156cf1422b2`  
		Last Modified: Tue, 09 Aug 2022 19:19:30 GMT  
		Size: 284.7 KB (284725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2fb79b7ce6b0abd6f8448fe016019030edc289f97327fe37b8dba13a5ef16a`  
		Last Modified: Wed, 10 Aug 2022 01:22:02 GMT  
		Size: 6.1 MB (6105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a97d2d84d94d10a270600330cb860dbdf068ba87de665aadd18f8e3535edea`  
		Last Modified: Wed, 10 Aug 2022 01:22:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c4c74a95e4772391d5c7a2016dd41623a306d27e25b7060be844fb9f4ee0e2`  
		Last Modified: Wed, 10 Aug 2022 01:22:01 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:c9193715ce031a4adacdc422577ed7d59bea06f261db5efa06148ada1e2622c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8569920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c888cfa4e2c0407f52481fb95e993322a6b8be9f4e93837e0852f771a40748f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:55:06 GMT
RUN apk add --no-cache ca-certificates
# Thu, 11 Aug 2022 00:00:28 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 11 Aug 2022 00:00:28 GMT
VOLUME [/var/lib/registry]
# Thu, 11 Aug 2022 00:00:28 GMT
EXPOSE 5000
# Thu, 11 Aug 2022 00:00:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 11 Aug 2022 00:00:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Aug 2022 00:00:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9c949f49fc8f526d6efc5da6670075476f51650be8b4471ba9b4b6e23b2ba`  
		Last Modified: Tue, 09 Aug 2022 19:19:26 GMT  
		Size: 284.7 KB (284675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c71446b2c03b8e2bc94167d3d3ec2a313dc829a959bb85d0daabd307248ba6`  
		Last Modified: Thu, 11 Aug 2022 00:00:48 GMT  
		Size: 5.7 MB (5670668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904c374b6acf45ffc25b5b1eba700fef9e2891ade700d450b86973aa5f4fd7d`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b946dba60cb877d6d42d9ce969d9c14f7223f5c5b527a019d5f333e7e862da6`  
		Last Modified: Thu, 11 Aug 2022 00:00:47 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:ad71f9315971b16106ad17df051520c0f32a2cfe8aa4aff257890a2dd88276d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8349558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f8e344076df43f3a4c364f38d787f90a79c6b4c969c84524f16574642cfc4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:04:00 GMT
RUN apk add --no-cache ca-certificates
# Tue, 19 Jul 2022 09:40:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 19 Jul 2022 09:40:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 19 Jul 2022 09:40:46 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Jul 2022 09:40:47 GMT
EXPOSE 5000
# Tue, 19 Jul 2022 09:40:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 19 Jul 2022 09:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 09:40:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f310150171570b715e2477d77efca60a48d1ddbc81587d89c7cbc2460c1ed361`  
		Last Modified: Mon, 18 Jul 2022 23:20:36 GMT  
		Size: 271.0 KB (270981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19f7609aebfc923d4c2b6d8167f2f830f9da00342ae8b849e1d20ffb195e662`  
		Last Modified: Tue, 19 Jul 2022 09:41:23 GMT  
		Size: 5.7 MB (5665659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a97de6c3e438f862a84820088419b83e84dfb6eda271bdfc6ddbd53c9d5b395`  
		Last Modified: Tue, 19 Jul 2022 09:41:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bd26b7e8bcd288a5dc04cb590110031fdc4216521991ee38323a219ac84ab6`  
		Last Modified: Tue, 19 Jul 2022 09:41:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:561ecbab74a78b52e52585ced90a46293b0923ad1faa380b73ab2335aee444c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8537219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4206ae70dd03980535dcc9ba7f04c973396cc8b4f324d44a1e706180b8ec068c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:07:56 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 05:40:20 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 05:40:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 05:40:22 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 05:40:23 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 05:40:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 05:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 05:40:26 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817a8a8f634c3a78b1a3b55a03335868971f2378932d3454ece4e3bfc5931675`  
		Last Modified: Tue, 09 Aug 2022 19:16:28 GMT  
		Size: 284.5 KB (284523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e865e4194320147cb54c543dfd5bd97d2121560564e3462ac4b8e96c4e6b5a`  
		Last Modified: Wed, 10 Aug 2022 05:40:45 GMT  
		Size: 5.5 MB (5544449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2cbf89aa09d2c7ecfb5662a97fa7836400a28119c987154fae927f41dde54`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0dc4e47315c6766f7a9f98a9020dc73cb7bc469272cb700be6d438a4ed8e93`  
		Last Modified: Wed, 10 Aug 2022 05:40:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:cc614c0da21cc46156655f767c1a99e8b9800135264736656d703f52acfa224b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8405964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355730cc5c16bb6422a7a4a9ae52935376e9a8de13adc44ba80ae79cf3d6edcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:01 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 02:18:23 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 02:18:24 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 02:18:24 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 02:18:24 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 02:18:25 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 02:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 02:18:25 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0369baf68c186e68d7c3cee256f5bc3a9351c6763ed88a03033834a5b942b700`  
		Last Modified: Tue, 09 Aug 2022 18:28:37 GMT  
		Size: 286.7 KB (286735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7899360365a91bf0dd803f7acfaba387f7f22011540b3d7686c96297666691f`  
		Last Modified: Wed, 10 Aug 2022 02:18:52 GMT  
		Size: 5.3 MB (5315294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7de731985617224f1bb2bc4be21f0443ccd1e9a0a2158cc4b227eeff291c2`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c665d99f8bec99576eb2116041d02399e02c1a6cf4975061f3c07b11c5c3eb`  
		Last Modified: Wed, 10 Aug 2022 02:18:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:12dce2d9bb3e725aa26281fd87cc175ce59ba5e838be21d4cb55d4dc1ce6347c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8687708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08713d331991e2b249b6538e92397edaa76a6dab591b20d5ffa87cdedf241844`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:45:21 GMT
RUN apk add --no-cache ca-certificates
# Wed, 10 Aug 2022 06:06:51 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 10 Aug 2022 06:06:52 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Aug 2022 06:06:52 GMT
EXPOSE 5000
# Wed, 10 Aug 2022 06:06:52 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 10 Aug 2022 06:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Aug 2022 06:06:52 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3e6b82e3d7aa395eb79202f28debe691c40472030a94ade061f395a44b1cfa`  
		Last Modified: Tue, 09 Aug 2022 18:55:04 GMT  
		Size: 284.9 KB (284946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042f30c5c9587a452cc286399cf6e33745ec1f847cb3d89d0d0853be8822559`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 5.8 MB (5811552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ff5faf84b39cd18d6d132da5b7f47ba503c19e93f7933a74dc77e6be802c90`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bbd7b4221680f3dc40fe532e93e45f093a469cb030e5edb7cec6c84e75cfc8`  
		Last Modified: Wed, 10 Aug 2022 06:07:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
