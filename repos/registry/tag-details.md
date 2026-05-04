<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:3`](#registry3)
-	[`registry:3.1`](#registry31)
-	[`registry:3.1.1`](#registry311)
-	[`registry:latest`](#registrylatest)

## `registry:3`

```console
$ docker pull registry@sha256:85347ed2ecde64161c7a4788a4d7d3dcc9d6f86f7be95834022e3c6a423a945a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3` - linux; amd64

```console
$ docker pull registry@sha256:6ad90ba0078c20cbdaa26b08aa2005a6ba409234f50f485d25eadd604704511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20186221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c26cd62311c2a4809cb93968ecda4aa30b8163e7a16977094ca0aee8441b19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:58 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:58 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:58 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:58 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:58 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a24b5445d2d943b847b335b71406c90b1c568226debe961c71b6fd139cf271`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 290.2 KB (290237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ddd084e87d6ac0b3a6602dffb29969642d22398589c4ea1bf8c683dc934bba`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 16.0 MB (16031184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c362d1d33f0d427a3b0ec006d425d38f8d1d5ab29ad039259f65a23b9c90a33`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b9845e5d5c48b57b99312c89adef03a6eac4cefa307274b3cfc4f66c6d503f`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:2a07507218eae0e94dfa5d9d59570e21b22dc3c1e7cf96960d494e7ff6d998fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadee70234ee62fa3e8074873bcc885776dfe3d18771c4378058070c5660168c`

```dockerfile
```

-	Layers:
	-	`sha256:7652fa2b866eb69ca9e9c5a44bda221b12b4b6238abd6d3b1727f9cbf62404d5`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 267.1 KB (267116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097321a3f414d7338a7e801ae19357a2f8bf665907b63795843d01785b46824a`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm variant v6

```console
$ docker pull registry@sha256:6eda9d920e7d14b232786d06e3a83ff31705f35221b048ba030267ac1fb6af71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b40a28a9ac35219f5a97b41c1ed733e8b559b47ccece2057c215851cee41217`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:00 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:00 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b4ac48c653dca9d6604f8ce6d6b76186ced9b9a9fcecd0ab35c3a8bd1c8365`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 291.0 KB (291025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ccce07ccf974917d2a1a6025869a022c6013b129c1ea640760aecf7442d9a1`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.9 MB (14911417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd64c49aac35b4e8abcae6ef071e7340ac2b7ec8eda501d1f030ce252d8a7623`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25290eb8b7ceaa371cf4b19695609b43857863c5e6a9cf00e8bfd8243e4484da`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:e7f635b44880b6478840a3dc9ba226213b38f05689de596240418bca5736658b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076765a923cad3a3c2c4f0ef1a744644e14913abdc9d3fba806df9147e8c8d79`

```dockerfile
```

-	Layers:
	-	`sha256:87727bd549b33e87f76cd496465607022c35b57a2659e3cd469e98d8175b82d8`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 14.2 KB (14203 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm variant v7

```console
$ docker pull registry@sha256:80266ad4b003068387ca2b76c38ef1a6e21930ed9757bcc47b8c9e2b9a05d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18466145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d480590a98497023fd4ad511532609b021ed300dec2bc02c2ee382211509c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72989bc19ff1c6c5b5044cab87d24180783b55d70acaaf43cc4a4c8c50baf3ab`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 290.2 KB (290162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc774303212be1c263aa9941888b4af883467554450fb3c245900eb0af7640`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.9 MB (14892248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bd9c58fad796fa21557d794ea2d0a801e03300e513cf2bde6fa1f75eab28bd`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2435387cf62986ec4ade238bcfed8af1a68841f3e77056773377cd8a7eff83`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:b684689cb7ce126225d3eb7f358a6f04a56071b10d24cd1f6a1175812ca21a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 KB (280155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc7853d30790f8e2f3d50479149727b410cf84b667e1d9c21805a341e13834`

```dockerfile
```

-	Layers:
	-	`sha256:c7117b26cd0fe632ce90fa4dbfb48e24ba5bb80ceb5510e1a18afce9d0390baa`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 265.7 KB (265738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae68f41325d327b2764a5940cd77db4089ca61fc8d2439aa637671cf1e5bf621`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4a3e4de10aba30740460958abb81e395a3c736d49e8189410eb14380b88c11be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18886954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a36fdc9ce411f6665445e961df69dbcc60de4668f534f55455da539304c3c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c935b29c51e392bacddfaf6deb2476f591ea96ba917344c92c8664406278b510`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 292.8 KB (292843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eadbc03e8b2d29dd8b9bd3575737e7d8419ed00986b92583ba55111a57d8772`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 MB (14393629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9f205913fcd5eabe90e22489c5f6be382b1c637b38d2b783070be268935d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:a9c94a614d3f3a894efe28a22b5654b747fe0d800f48fbd7b48965dd4ad7253c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 KB (280965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a5f73b7736dcca68db190cdef1ffec13d67d094de604901ee2ca95b85813f`

```dockerfile
```

-	Layers:
	-	`sha256:0ce323f5a13432bb8ce2dd76a4d21a843f2bca43d4b0d1311245ec685627d783`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 266.5 KB (266522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d9f54ea065b42af0aedf1ca1c3e913a971da9088aa2eb6bf384cadad633c5`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; ppc64le

```console
$ docker pull registry@sha256:19e9c844b8ccaf249ba0350c94f31fa3c5241800e5b77435b0ca40252da548e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18440061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57cd97e77ff406b4ca257a7af78484be4069d094fc3433fd0e759fbb54a69d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:07 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:10 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:10 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:10 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc28442c29f863e63d326f2907fc0ebc5b574c45a36e3631e9ad97ca2840eb`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 14.3 MB (14315156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df7398540bb85fe5e156d9f4b022729383e75cd7279f64d78cc6029b8766505`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccab6aead6769b98571d18752c821424b4630cb83ba2d499fff8227d6ddf5221`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:4db3c66f598bc871d1329d1819a54c3827d8780c811de81b4c196c475644470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fa3d9fdfcc8bf48b49750bee164192145759d6cf6269cc6aae4efc5a536e3b`

```dockerfile
```

-	Layers:
	-	`sha256:fea3fe7902245d6d26f51efe7023a31b720d5fba6def9442fa5abb50c5861313`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 266.5 KB (266499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40feac9cc7469e3deeacf3582d5231cb441df8f07cb7200c3cb6db3cca12485`  
		Last Modified: Mon, 04 May 2026 19:09:26 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; riscv64

```console
$ docker pull registry@sha256:6bac5ab784ef1271ea9c19fe949e249e46781a8de8e74f5d5eee4d2333d83e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19195319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1d893b9dfa1fceed9ded71ee8776f67539424e006b0c95b79818cb4e148f8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:59 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:59 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7229a593c1ad909b80cb6562febfcb3c3ae614360f60e39f3df6b630c4b88f`  
		Last Modified: Mon, 04 May 2026 19:11:00 GMT  
		Size: 15.3 MB (15316494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd35c839b775367c12cccd08b74875815de87b7f413f1cf27d6c57422475602`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:733beffa3194e41d1ee399b26ad63dc14aa216b30a95b9717c8d08a45017a4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f0a1e30786f79a24c7473ae1e05cf0721d345db3b4eda3060c12905b1c824`

```dockerfile
```

-	Layers:
	-	`sha256:96f06bc2cdfa4dcdd98ff60faffcf5f6e32bcd776b2bf063527786625546bbfe`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 266.5 KB (266495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57212effb84c519d6d4d843f6bb8a8d3475a11839fe208599208326c2d7541a4`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; s390x

```console
$ docker pull registry@sha256:f68ddb2c80f3c32bfdad556dcfc964593dafdfdc35e7eea8a7979171b3eebeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19379303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f99cec84ffb3966f1d7ad6e8562eca3c81abd082fe9e7f85efab8fa45f453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:09 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:09 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:09 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:09 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb85227a6d474422f642a20f11c0f9c523b2abb74d9032c4b7170dedd36bf4`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d358963776d769c7f2736c5ec9489fc841617d8221a1b6dc26d17920d5f30d1`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 15.4 MB (15361010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beb4957366145b84e0d246c216fa7b2591444ea2e5b8d27f863f855eba88fd5`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11a075a97171b27116027cc5c59122865ba95ff08afa513e34e3a43fe61666`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:1d584ba4a10b541bd7e17651d8fde859bdd73b460b18af12e5bf7e6d65223f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11754b8ed2807ffd1282bf4d4ec482636bf76830f3df5a8f4cab580d3030177a`

```dockerfile
```

-	Layers:
	-	`sha256:dae3237806cf33c56b83d5c14b648ec1b1bfd86f4d04926cada543d227029d68`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 266.5 KB (266465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92c5aa8ad1786b40e7559b569736c824e8f5cfc0030d96b3f802f11642d7271`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.1`

```console
$ docker pull registry@sha256:85347ed2ecde64161c7a4788a4d7d3dcc9d6f86f7be95834022e3c6a423a945a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.1` - linux; amd64

```console
$ docker pull registry@sha256:6ad90ba0078c20cbdaa26b08aa2005a6ba409234f50f485d25eadd604704511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20186221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c26cd62311c2a4809cb93968ecda4aa30b8163e7a16977094ca0aee8441b19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:58 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:58 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:58 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:58 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:58 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a24b5445d2d943b847b335b71406c90b1c568226debe961c71b6fd139cf271`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 290.2 KB (290237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ddd084e87d6ac0b3a6602dffb29969642d22398589c4ea1bf8c683dc934bba`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 16.0 MB (16031184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c362d1d33f0d427a3b0ec006d425d38f8d1d5ab29ad039259f65a23b9c90a33`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b9845e5d5c48b57b99312c89adef03a6eac4cefa307274b3cfc4f66c6d503f`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1` - unknown; unknown

```console
$ docker pull registry@sha256:2a07507218eae0e94dfa5d9d59570e21b22dc3c1e7cf96960d494e7ff6d998fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadee70234ee62fa3e8074873bcc885776dfe3d18771c4378058070c5660168c`

```dockerfile
```

-	Layers:
	-	`sha256:7652fa2b866eb69ca9e9c5a44bda221b12b4b6238abd6d3b1727f9cbf62404d5`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 267.1 KB (267116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097321a3f414d7338a7e801ae19357a2f8bf665907b63795843d01785b46824a`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:6eda9d920e7d14b232786d06e3a83ff31705f35221b048ba030267ac1fb6af71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b40a28a9ac35219f5a97b41c1ed733e8b559b47ccece2057c215851cee41217`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:00 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:00 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b4ac48c653dca9d6604f8ce6d6b76186ced9b9a9fcecd0ab35c3a8bd1c8365`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 291.0 KB (291025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ccce07ccf974917d2a1a6025869a022c6013b129c1ea640760aecf7442d9a1`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.9 MB (14911417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd64c49aac35b4e8abcae6ef071e7340ac2b7ec8eda501d1f030ce252d8a7623`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25290eb8b7ceaa371cf4b19695609b43857863c5e6a9cf00e8bfd8243e4484da`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1` - unknown; unknown

```console
$ docker pull registry@sha256:e7f635b44880b6478840a3dc9ba226213b38f05689de596240418bca5736658b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076765a923cad3a3c2c4f0ef1a744644e14913abdc9d3fba806df9147e8c8d79`

```dockerfile
```

-	Layers:
	-	`sha256:87727bd549b33e87f76cd496465607022c35b57a2659e3cd469e98d8175b82d8`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 14.2 KB (14203 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:80266ad4b003068387ca2b76c38ef1a6e21930ed9757bcc47b8c9e2b9a05d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18466145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d480590a98497023fd4ad511532609b021ed300dec2bc02c2ee382211509c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72989bc19ff1c6c5b5044cab87d24180783b55d70acaaf43cc4a4c8c50baf3ab`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 290.2 KB (290162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc774303212be1c263aa9941888b4af883467554450fb3c245900eb0af7640`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.9 MB (14892248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bd9c58fad796fa21557d794ea2d0a801e03300e513cf2bde6fa1f75eab28bd`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2435387cf62986ec4ade238bcfed8af1a68841f3e77056773377cd8a7eff83`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1` - unknown; unknown

```console
$ docker pull registry@sha256:b684689cb7ce126225d3eb7f358a6f04a56071b10d24cd1f6a1175812ca21a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 KB (280155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc7853d30790f8e2f3d50479149727b410cf84b667e1d9c21805a341e13834`

```dockerfile
```

-	Layers:
	-	`sha256:c7117b26cd0fe632ce90fa4dbfb48e24ba5bb80ceb5510e1a18afce9d0390baa`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 265.7 KB (265738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae68f41325d327b2764a5940cd77db4089ca61fc8d2439aa637671cf1e5bf621`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4a3e4de10aba30740460958abb81e395a3c736d49e8189410eb14380b88c11be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18886954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a36fdc9ce411f6665445e961df69dbcc60de4668f534f55455da539304c3c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c935b29c51e392bacddfaf6deb2476f591ea96ba917344c92c8664406278b510`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 292.8 KB (292843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eadbc03e8b2d29dd8b9bd3575737e7d8419ed00986b92583ba55111a57d8772`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 MB (14393629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9f205913fcd5eabe90e22489c5f6be382b1c637b38d2b783070be268935d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1` - unknown; unknown

```console
$ docker pull registry@sha256:a9c94a614d3f3a894efe28a22b5654b747fe0d800f48fbd7b48965dd4ad7253c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 KB (280965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a5f73b7736dcca68db190cdef1ffec13d67d094de604901ee2ca95b85813f`

```dockerfile
```

-	Layers:
	-	`sha256:0ce323f5a13432bb8ce2dd76a4d21a843f2bca43d4b0d1311245ec685627d783`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 266.5 KB (266522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d9f54ea065b42af0aedf1ca1c3e913a971da9088aa2eb6bf384cadad633c5`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1` - linux; ppc64le

```console
$ docker pull registry@sha256:19e9c844b8ccaf249ba0350c94f31fa3c5241800e5b77435b0ca40252da548e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18440061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57cd97e77ff406b4ca257a7af78484be4069d094fc3433fd0e759fbb54a69d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:07 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:10 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:10 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:10 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc28442c29f863e63d326f2907fc0ebc5b574c45a36e3631e9ad97ca2840eb`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 14.3 MB (14315156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df7398540bb85fe5e156d9f4b022729383e75cd7279f64d78cc6029b8766505`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccab6aead6769b98571d18752c821424b4630cb83ba2d499fff8227d6ddf5221`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1` - unknown; unknown

```console
$ docker pull registry@sha256:4db3c66f598bc871d1329d1819a54c3827d8780c811de81b4c196c475644470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fa3d9fdfcc8bf48b49750bee164192145759d6cf6269cc6aae4efc5a536e3b`

```dockerfile
```

-	Layers:
	-	`sha256:fea3fe7902245d6d26f51efe7023a31b720d5fba6def9442fa5abb50c5861313`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 266.5 KB (266499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40feac9cc7469e3deeacf3582d5231cb441df8f07cb7200c3cb6db3cca12485`  
		Last Modified: Mon, 04 May 2026 19:09:26 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1` - linux; riscv64

```console
$ docker pull registry@sha256:6bac5ab784ef1271ea9c19fe949e249e46781a8de8e74f5d5eee4d2333d83e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19195319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1d893b9dfa1fceed9ded71ee8776f67539424e006b0c95b79818cb4e148f8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:59 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:59 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7229a593c1ad909b80cb6562febfcb3c3ae614360f60e39f3df6b630c4b88f`  
		Last Modified: Mon, 04 May 2026 19:11:00 GMT  
		Size: 15.3 MB (15316494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd35c839b775367c12cccd08b74875815de87b7f413f1cf27d6c57422475602`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1` - unknown; unknown

```console
$ docker pull registry@sha256:733beffa3194e41d1ee399b26ad63dc14aa216b30a95b9717c8d08a45017a4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f0a1e30786f79a24c7473ae1e05cf0721d345db3b4eda3060c12905b1c824`

```dockerfile
```

-	Layers:
	-	`sha256:96f06bc2cdfa4dcdd98ff60faffcf5f6e32bcd776b2bf063527786625546bbfe`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 266.5 KB (266495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57212effb84c519d6d4d843f6bb8a8d3475a11839fe208599208326c2d7541a4`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1` - linux; s390x

```console
$ docker pull registry@sha256:f68ddb2c80f3c32bfdad556dcfc964593dafdfdc35e7eea8a7979171b3eebeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19379303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f99cec84ffb3966f1d7ad6e8562eca3c81abd082fe9e7f85efab8fa45f453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:09 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:09 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:09 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:09 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb85227a6d474422f642a20f11c0f9c523b2abb74d9032c4b7170dedd36bf4`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d358963776d769c7f2736c5ec9489fc841617d8221a1b6dc26d17920d5f30d1`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 15.4 MB (15361010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beb4957366145b84e0d246c216fa7b2591444ea2e5b8d27f863f855eba88fd5`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11a075a97171b27116027cc5c59122865ba95ff08afa513e34e3a43fe61666`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1` - unknown; unknown

```console
$ docker pull registry@sha256:1d584ba4a10b541bd7e17651d8fde859bdd73b460b18af12e5bf7e6d65223f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11754b8ed2807ffd1282bf4d4ec482636bf76830f3df5a8f4cab580d3030177a`

```dockerfile
```

-	Layers:
	-	`sha256:dae3237806cf33c56b83d5c14b648ec1b1bfd86f4d04926cada543d227029d68`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 266.5 KB (266465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92c5aa8ad1786b40e7559b569736c824e8f5cfc0030d96b3f802f11642d7271`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.1.1`

```console
$ docker pull registry@sha256:85347ed2ecde64161c7a4788a4d7d3dcc9d6f86f7be95834022e3c6a423a945a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.1.1` - linux; amd64

```console
$ docker pull registry@sha256:6ad90ba0078c20cbdaa26b08aa2005a6ba409234f50f485d25eadd604704511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20186221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c26cd62311c2a4809cb93968ecda4aa30b8163e7a16977094ca0aee8441b19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:58 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:58 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:58 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:58 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:58 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a24b5445d2d943b847b335b71406c90b1c568226debe961c71b6fd139cf271`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 290.2 KB (290237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ddd084e87d6ac0b3a6602dffb29969642d22398589c4ea1bf8c683dc934bba`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 16.0 MB (16031184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c362d1d33f0d427a3b0ec006d425d38f8d1d5ab29ad039259f65a23b9c90a33`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b9845e5d5c48b57b99312c89adef03a6eac4cefa307274b3cfc4f66c6d503f`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1.1` - unknown; unknown

```console
$ docker pull registry@sha256:2a07507218eae0e94dfa5d9d59570e21b22dc3c1e7cf96960d494e7ff6d998fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadee70234ee62fa3e8074873bcc885776dfe3d18771c4378058070c5660168c`

```dockerfile
```

-	Layers:
	-	`sha256:7652fa2b866eb69ca9e9c5a44bda221b12b4b6238abd6d3b1727f9cbf62404d5`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 267.1 KB (267116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097321a3f414d7338a7e801ae19357a2f8bf665907b63795843d01785b46824a`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:6eda9d920e7d14b232786d06e3a83ff31705f35221b048ba030267ac1fb6af71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b40a28a9ac35219f5a97b41c1ed733e8b559b47ccece2057c215851cee41217`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:00 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:00 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b4ac48c653dca9d6604f8ce6d6b76186ced9b9a9fcecd0ab35c3a8bd1c8365`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 291.0 KB (291025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ccce07ccf974917d2a1a6025869a022c6013b129c1ea640760aecf7442d9a1`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.9 MB (14911417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd64c49aac35b4e8abcae6ef071e7340ac2b7ec8eda501d1f030ce252d8a7623`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25290eb8b7ceaa371cf4b19695609b43857863c5e6a9cf00e8bfd8243e4484da`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1.1` - unknown; unknown

```console
$ docker pull registry@sha256:e7f635b44880b6478840a3dc9ba226213b38f05689de596240418bca5736658b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076765a923cad3a3c2c4f0ef1a744644e14913abdc9d3fba806df9147e8c8d79`

```dockerfile
```

-	Layers:
	-	`sha256:87727bd549b33e87f76cd496465607022c35b57a2659e3cd469e98d8175b82d8`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 14.2 KB (14203 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:80266ad4b003068387ca2b76c38ef1a6e21930ed9757bcc47b8c9e2b9a05d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18466145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d480590a98497023fd4ad511532609b021ed300dec2bc02c2ee382211509c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72989bc19ff1c6c5b5044cab87d24180783b55d70acaaf43cc4a4c8c50baf3ab`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 290.2 KB (290162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc774303212be1c263aa9941888b4af883467554450fb3c245900eb0af7640`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.9 MB (14892248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bd9c58fad796fa21557d794ea2d0a801e03300e513cf2bde6fa1f75eab28bd`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2435387cf62986ec4ade238bcfed8af1a68841f3e77056773377cd8a7eff83`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1.1` - unknown; unknown

```console
$ docker pull registry@sha256:b684689cb7ce126225d3eb7f358a6f04a56071b10d24cd1f6a1175812ca21a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 KB (280155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc7853d30790f8e2f3d50479149727b410cf84b667e1d9c21805a341e13834`

```dockerfile
```

-	Layers:
	-	`sha256:c7117b26cd0fe632ce90fa4dbfb48e24ba5bb80ceb5510e1a18afce9d0390baa`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 265.7 KB (265738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae68f41325d327b2764a5940cd77db4089ca61fc8d2439aa637671cf1e5bf621`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4a3e4de10aba30740460958abb81e395a3c736d49e8189410eb14380b88c11be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18886954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a36fdc9ce411f6665445e961df69dbcc60de4668f534f55455da539304c3c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c935b29c51e392bacddfaf6deb2476f591ea96ba917344c92c8664406278b510`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 292.8 KB (292843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eadbc03e8b2d29dd8b9bd3575737e7d8419ed00986b92583ba55111a57d8772`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 MB (14393629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9f205913fcd5eabe90e22489c5f6be382b1c637b38d2b783070be268935d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1.1` - unknown; unknown

```console
$ docker pull registry@sha256:a9c94a614d3f3a894efe28a22b5654b747fe0d800f48fbd7b48965dd4ad7253c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 KB (280965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a5f73b7736dcca68db190cdef1ffec13d67d094de604901ee2ca95b85813f`

```dockerfile
```

-	Layers:
	-	`sha256:0ce323f5a13432bb8ce2dd76a4d21a843f2bca43d4b0d1311245ec685627d783`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 266.5 KB (266522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d9f54ea065b42af0aedf1ca1c3e913a971da9088aa2eb6bf384cadad633c5`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1.1` - linux; ppc64le

```console
$ docker pull registry@sha256:19e9c844b8ccaf249ba0350c94f31fa3c5241800e5b77435b0ca40252da548e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18440061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57cd97e77ff406b4ca257a7af78484be4069d094fc3433fd0e759fbb54a69d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:07 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:10 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:10 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:10 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc28442c29f863e63d326f2907fc0ebc5b574c45a36e3631e9ad97ca2840eb`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 14.3 MB (14315156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df7398540bb85fe5e156d9f4b022729383e75cd7279f64d78cc6029b8766505`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccab6aead6769b98571d18752c821424b4630cb83ba2d499fff8227d6ddf5221`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1.1` - unknown; unknown

```console
$ docker pull registry@sha256:4db3c66f598bc871d1329d1819a54c3827d8780c811de81b4c196c475644470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fa3d9fdfcc8bf48b49750bee164192145759d6cf6269cc6aae4efc5a536e3b`

```dockerfile
```

-	Layers:
	-	`sha256:fea3fe7902245d6d26f51efe7023a31b720d5fba6def9442fa5abb50c5861313`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 266.5 KB (266499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40feac9cc7469e3deeacf3582d5231cb441df8f07cb7200c3cb6db3cca12485`  
		Last Modified: Mon, 04 May 2026 19:09:26 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1.1` - linux; riscv64

```console
$ docker pull registry@sha256:6bac5ab784ef1271ea9c19fe949e249e46781a8de8e74f5d5eee4d2333d83e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19195319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1d893b9dfa1fceed9ded71ee8776f67539424e006b0c95b79818cb4e148f8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:59 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:59 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7229a593c1ad909b80cb6562febfcb3c3ae614360f60e39f3df6b630c4b88f`  
		Last Modified: Mon, 04 May 2026 19:11:00 GMT  
		Size: 15.3 MB (15316494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd35c839b775367c12cccd08b74875815de87b7f413f1cf27d6c57422475602`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1.1` - unknown; unknown

```console
$ docker pull registry@sha256:733beffa3194e41d1ee399b26ad63dc14aa216b30a95b9717c8d08a45017a4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f0a1e30786f79a24c7473ae1e05cf0721d345db3b4eda3060c12905b1c824`

```dockerfile
```

-	Layers:
	-	`sha256:96f06bc2cdfa4dcdd98ff60faffcf5f6e32bcd776b2bf063527786625546bbfe`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 266.5 KB (266495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57212effb84c519d6d4d843f6bb8a8d3475a11839fe208599208326c2d7541a4`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.1.1` - linux; s390x

```console
$ docker pull registry@sha256:f68ddb2c80f3c32bfdad556dcfc964593dafdfdc35e7eea8a7979171b3eebeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19379303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f99cec84ffb3966f1d7ad6e8562eca3c81abd082fe9e7f85efab8fa45f453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:09 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:09 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:09 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:09 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb85227a6d474422f642a20f11c0f9c523b2abb74d9032c4b7170dedd36bf4`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d358963776d769c7f2736c5ec9489fc841617d8221a1b6dc26d17920d5f30d1`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 15.4 MB (15361010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beb4957366145b84e0d246c216fa7b2591444ea2e5b8d27f863f855eba88fd5`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11a075a97171b27116027cc5c59122865ba95ff08afa513e34e3a43fe61666`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.1.1` - unknown; unknown

```console
$ docker pull registry@sha256:1d584ba4a10b541bd7e17651d8fde859bdd73b460b18af12e5bf7e6d65223f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11754b8ed2807ffd1282bf4d4ec482636bf76830f3df5a8f4cab580d3030177a`

```dockerfile
```

-	Layers:
	-	`sha256:dae3237806cf33c56b83d5c14b648ec1b1bfd86f4d04926cada543d227029d68`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 266.5 KB (266465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92c5aa8ad1786b40e7559b569736c824e8f5cfc0030d96b3f802f11642d7271`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:85347ed2ecde64161c7a4788a4d7d3dcc9d6f86f7be95834022e3c6a423a945a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:6ad90ba0078c20cbdaa26b08aa2005a6ba409234f50f485d25eadd604704511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20186221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c26cd62311c2a4809cb93968ecda4aa30b8163e7a16977094ca0aee8441b19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:58 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:58 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:58 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:58 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:58 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a24b5445d2d943b847b335b71406c90b1c568226debe961c71b6fd139cf271`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 290.2 KB (290237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ddd084e87d6ac0b3a6602dffb29969642d22398589c4ea1bf8c683dc934bba`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 16.0 MB (16031184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c362d1d33f0d427a3b0ec006d425d38f8d1d5ab29ad039259f65a23b9c90a33`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b9845e5d5c48b57b99312c89adef03a6eac4cefa307274b3cfc4f66c6d503f`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:2a07507218eae0e94dfa5d9d59570e21b22dc3c1e7cf96960d494e7ff6d998fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadee70234ee62fa3e8074873bcc885776dfe3d18771c4378058070c5660168c`

```dockerfile
```

-	Layers:
	-	`sha256:7652fa2b866eb69ca9e9c5a44bda221b12b4b6238abd6d3b1727f9cbf62404d5`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 267.1 KB (267116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097321a3f414d7338a7e801ae19357a2f8bf665907b63795843d01785b46824a`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:6eda9d920e7d14b232786d06e3a83ff31705f35221b048ba030267ac1fb6af71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b40a28a9ac35219f5a97b41c1ed733e8b559b47ccece2057c215851cee41217`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:00 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:00 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b4ac48c653dca9d6604f8ce6d6b76186ced9b9a9fcecd0ab35c3a8bd1c8365`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 291.0 KB (291025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ccce07ccf974917d2a1a6025869a022c6013b129c1ea640760aecf7442d9a1`  
		Last Modified: Mon, 04 May 2026 19:10:06 GMT  
		Size: 14.9 MB (14911417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd64c49aac35b4e8abcae6ef071e7340ac2b7ec8eda501d1f030ce252d8a7623`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25290eb8b7ceaa371cf4b19695609b43857863c5e6a9cf00e8bfd8243e4484da`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:e7f635b44880b6478840a3dc9ba226213b38f05689de596240418bca5736658b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076765a923cad3a3c2c4f0ef1a744644e14913abdc9d3fba806df9147e8c8d79`

```dockerfile
```

-	Layers:
	-	`sha256:87727bd549b33e87f76cd496465607022c35b57a2659e3cd469e98d8175b82d8`  
		Last Modified: Mon, 04 May 2026 19:10:05 GMT  
		Size: 14.2 KB (14203 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:80266ad4b003068387ca2b76c38ef1a6e21930ed9757bcc47b8c9e2b9a05d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18466145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d480590a98497023fd4ad511532609b021ed300dec2bc02c2ee382211509c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72989bc19ff1c6c5b5044cab87d24180783b55d70acaaf43cc4a4c8c50baf3ab`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 290.2 KB (290162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc774303212be1c263aa9941888b4af883467554450fb3c245900eb0af7640`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.9 MB (14892248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bd9c58fad796fa21557d794ea2d0a801e03300e513cf2bde6fa1f75eab28bd`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2435387cf62986ec4ade238bcfed8af1a68841f3e77056773377cd8a7eff83`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:b684689cb7ce126225d3eb7f358a6f04a56071b10d24cd1f6a1175812ca21a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 KB (280155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc7853d30790f8e2f3d50479149727b410cf84b667e1d9c21805a341e13834`

```dockerfile
```

-	Layers:
	-	`sha256:c7117b26cd0fe632ce90fa4dbfb48e24ba5bb80ceb5510e1a18afce9d0390baa`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 265.7 KB (265738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae68f41325d327b2764a5940cd77db4089ca61fc8d2439aa637671cf1e5bf621`  
		Last Modified: Mon, 04 May 2026 19:10:11 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4a3e4de10aba30740460958abb81e395a3c736d49e8189410eb14380b88c11be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18886954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a36fdc9ce411f6665445e961df69dbcc60de4668f534f55455da539304c3c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:10:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:10:02 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:10:02 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:02 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:02 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:02 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c935b29c51e392bacddfaf6deb2476f591ea96ba917344c92c8664406278b510`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 292.8 KB (292843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eadbc03e8b2d29dd8b9bd3575737e7d8419ed00986b92583ba55111a57d8772`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 MB (14393629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9f205913fcd5eabe90e22489c5f6be382b1c637b38d2b783070be268935d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:a9c94a614d3f3a894efe28a22b5654b747fe0d800f48fbd7b48965dd4ad7253c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 KB (280965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a5f73b7736dcca68db190cdef1ffec13d67d094de604901ee2ca95b85813f`

```dockerfile
```

-	Layers:
	-	`sha256:0ce323f5a13432bb8ce2dd76a4d21a843f2bca43d4b0d1311245ec685627d783`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 266.5 KB (266522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d9f54ea065b42af0aedf1ca1c3e913a971da9088aa2eb6bf384cadad633c5`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:19e9c844b8ccaf249ba0350c94f31fa3c5241800e5b77435b0ca40252da548e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18440061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57cd97e77ff406b4ca257a7af78484be4069d094fc3433fd0e759fbb54a69d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:07 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:10 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:10 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:10 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc28442c29f863e63d326f2907fc0ebc5b574c45a36e3631e9ad97ca2840eb`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 14.3 MB (14315156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df7398540bb85fe5e156d9f4b022729383e75cd7279f64d78cc6029b8766505`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccab6aead6769b98571d18752c821424b4630cb83ba2d499fff8227d6ddf5221`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:4db3c66f598bc871d1329d1819a54c3827d8780c811de81b4c196c475644470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fa3d9fdfcc8bf48b49750bee164192145759d6cf6269cc6aae4efc5a536e3b`

```dockerfile
```

-	Layers:
	-	`sha256:fea3fe7902245d6d26f51efe7023a31b720d5fba6def9442fa5abb50c5861313`  
		Last Modified: Mon, 04 May 2026 19:09:27 GMT  
		Size: 266.5 KB (266499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40feac9cc7469e3deeacf3582d5231cb441df8f07cb7200c3cb6db3cca12485`  
		Last Modified: Mon, 04 May 2026 19:09:26 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; riscv64

```console
$ docker pull registry@sha256:6bac5ab784ef1271ea9c19fe949e249e46781a8de8e74f5d5eee4d2333d83e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19195319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1d893b9dfa1fceed9ded71ee8776f67539424e006b0c95b79818cb4e148f8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:59 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:59 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7229a593c1ad909b80cb6562febfcb3c3ae614360f60e39f3df6b630c4b88f`  
		Last Modified: Mon, 04 May 2026 19:11:00 GMT  
		Size: 15.3 MB (15316494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd35c839b775367c12cccd08b74875815de87b7f413f1cf27d6c57422475602`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:733beffa3194e41d1ee399b26ad63dc14aa216b30a95b9717c8d08a45017a4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f0a1e30786f79a24c7473ae1e05cf0721d345db3b4eda3060c12905b1c824`

```dockerfile
```

-	Layers:
	-	`sha256:96f06bc2cdfa4dcdd98ff60faffcf5f6e32bcd776b2bf063527786625546bbfe`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 266.5 KB (266495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57212effb84c519d6d4d843f6bb8a8d3475a11839fe208599208326c2d7541a4`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:f68ddb2c80f3c32bfdad556dcfc964593dafdfdc35e7eea8a7979171b3eebeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19379303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f99cec84ffb3966f1d7ad6e8562eca3c81abd082fe9e7f85efab8fa45f453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:09 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:09 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:09:09 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:09:09 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:09:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:09:09 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb85227a6d474422f642a20f11c0f9c523b2abb74d9032c4b7170dedd36bf4`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d358963776d769c7f2736c5ec9489fc841617d8221a1b6dc26d17920d5f30d1`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 15.4 MB (15361010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beb4957366145b84e0d246c216fa7b2591444ea2e5b8d27f863f855eba88fd5`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11a075a97171b27116027cc5c59122865ba95ff08afa513e34e3a43fe61666`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1d584ba4a10b541bd7e17651d8fde859bdd73b460b18af12e5bf7e6d65223f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11754b8ed2807ffd1282bf4d4ec482636bf76830f3df5a8f4cab580d3030177a`

```dockerfile
```

-	Layers:
	-	`sha256:dae3237806cf33c56b83d5c14b648ec1b1bfd86f4d04926cada543d227029d68`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 266.5 KB (266465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92c5aa8ad1786b40e7559b569736c824e8f5cfc0030d96b3f802f11642d7271`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json
