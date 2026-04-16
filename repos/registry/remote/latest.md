## `registry:latest`

```console
$ docker pull registry@sha256:b0f3668eb14daa3089aee66b4afd65bf2c2065439d6b5b6357bd3ba711fcf5bd
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
$ docker pull registry@sha256:2e0bc2c0de49167e60e6e00dbc307707cdfe8380e9243b7c582297ece2f71315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20187413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57b533ccae55b072a3ff7627f302f042502f3701ee5442ef62aaac718dc5f72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:21:59 GMT
RUN set -eux; 	version='3.1.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='c69f2b8778c5357a77f6b41730d94d5f0b2b7cf54534040a06af5f0a70a731b2' ;; 		aarch64) arch='arm64';   sha256='f5527b7ed356767afb8a616e7b9423ef161b470e3674893e395e2a4e656deb1c' ;; 		armhf)   arch='armv6';   sha256='2c9a44ea1c289bade76770de459c437dde0bea3b44a3e7555264a63707e71470' ;; 		armv7)   arch='armv7';   sha256='0217d5704cd0be893320e686ca6bb7341991d9ed23251ac1265301994a890b6f' ;; 		ppc64le) arch='ppc64le'; sha256='1dc0fc28f368dd2d3b485f1bc7f9e5a6cb2421cf8fa94aade30fc334a362ae47' ;; 		s390x)   arch='s390x';   sha256='cbe535d6d70e5d9b6c160a6c52445eb9c90af57e12e2b5d377d1263077ae741e' ;; 		riscv64) arch='riscv64'; sha256='77cd50cd517758a5de09391d4cbda47e64caf1b67ba07413fbfbfeffed6de444' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 15 Apr 2026 20:21:59 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 15 Apr 2026 20:21:59 GMT
ENV OTEL_TRACES_EXPORTER=none
# Wed, 15 Apr 2026 20:21:59 GMT
VOLUME [/var/lib/registry]
# Wed, 15 Apr 2026 20:21:59 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 15 Apr 2026 20:21:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:21:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:59 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb496381bf96a08576a8320f7ff7202e580d0da89ae78f7abc411f7c21974eb`  
		Last Modified: Wed, 15 Apr 2026 20:22:06 GMT  
		Size: 290.2 KB (290244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d40529a15df09d26ebad4259e67d2df9bd71e49c6d353df1a2ea2379520599`  
		Last Modified: Wed, 15 Apr 2026 20:22:07 GMT  
		Size: 16.0 MB (16032369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a873a8475f334c8cd45e70dc8307d27c80af9f942c76be0e79fbf28b5acb84d`  
		Last Modified: Wed, 15 Apr 2026 20:22:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a63e4991477efc579e67e6e6508f77607f39959f39ca545907ff8260df861`  
		Last Modified: Wed, 15 Apr 2026 20:22:07 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:27b02937db3498296e14230f72097c5538211fad2e8e19b760e49045b73e5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf5c8400d9ad697b5f5a16a3046bfc3dfe5780cd627e6eff44b448b1e8e34f4`

```dockerfile
```

-	Layers:
	-	`sha256:1dcff396b6c8f918aee30a850a1278e7219e81c79c03779305eaa7cb7f89b5c8`  
		Last Modified: Wed, 15 Apr 2026 20:22:06 GMT  
		Size: 267.1 KB (267114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fb53714865c8efe46ea85bc07b94947d52e9fda35863d6ccb5d4adbf345c22`  
		Last Modified: Wed, 15 Apr 2026 20:22:06 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:c3a6c7fe4080da940979d8a6067fd0829f5353af002a989e5ca2ce0cd246de3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18774009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da8f26a296cd1e2de9b7ce7e6690053fe421c385477faf72753cddc230e3255`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:30:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:30:48 GMT
RUN set -eux; 	version='3.1.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='c69f2b8778c5357a77f6b41730d94d5f0b2b7cf54534040a06af5f0a70a731b2' ;; 		aarch64) arch='arm64';   sha256='f5527b7ed356767afb8a616e7b9423ef161b470e3674893e395e2a4e656deb1c' ;; 		armhf)   arch='armv6';   sha256='2c9a44ea1c289bade76770de459c437dde0bea3b44a3e7555264a63707e71470' ;; 		armv7)   arch='armv7';   sha256='0217d5704cd0be893320e686ca6bb7341991d9ed23251ac1265301994a890b6f' ;; 		ppc64le) arch='ppc64le'; sha256='1dc0fc28f368dd2d3b485f1bc7f9e5a6cb2421cf8fa94aade30fc334a362ae47' ;; 		s390x)   arch='s390x';   sha256='cbe535d6d70e5d9b6c160a6c52445eb9c90af57e12e2b5d377d1263077ae741e' ;; 		riscv64) arch='riscv64'; sha256='77cd50cd517758a5de09391d4cbda47e64caf1b67ba07413fbfbfeffed6de444' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 15 Apr 2026 20:30:48 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 15 Apr 2026 20:30:48 GMT
ENV OTEL_TRACES_EXPORTER=none
# Wed, 15 Apr 2026 20:30:48 GMT
VOLUME [/var/lib/registry]
# Wed, 15 Apr 2026 20:30:48 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 15 Apr 2026 20:30:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:30:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:30:48 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c5793b7330baba2bdbdcfc15c9c30a01c808c080ac6caa02bf3b5585d2f0b`  
		Last Modified: Wed, 15 Apr 2026 20:30:53 GMT  
		Size: 291.0 KB (291020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a803f642b9610a88267f90c72d4ef2dcdd1466a02ffff081253e0c8cb007518`  
		Last Modified: Wed, 15 Apr 2026 20:30:53 GMT  
		Size: 14.9 MB (14910516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429976651e6fd4e0807c8e4adf51e14be417e47d99e54d2661038b96054f20ee`  
		Last Modified: Wed, 15 Apr 2026 20:30:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0349c1b4a28ea362e586a01485dedd33cd0a753883d682880bc03002670d1d`  
		Last Modified: Wed, 15 Apr 2026 20:30:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:4ccacfcb8f7433a1427bdc99a7efbd43b48798717110bb7a00302746c1a60db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feffe47d077ab3207ff778e8feaa71fd0cf8937b9e260568bb3066021e7026ae`

```dockerfile
```

-	Layers:
	-	`sha256:002c2aea5f8bcd9517bee7160dae66e52143259ea3574bfe18a3b697bcebf24b`  
		Last Modified: Wed, 15 Apr 2026 20:30:53 GMT  
		Size: 14.2 KB (14203 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:0ed5c9f33cda0f455115c3c07f74fb992b9aa81649bdfd30bf82b48998045a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18469652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1598e19a2d740c5f6aea840a04243ddf71348df09705980206264f777e6db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:30:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
RUN set -eux; 	version='3.1.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='c69f2b8778c5357a77f6b41730d94d5f0b2b7cf54534040a06af5f0a70a731b2' ;; 		aarch64) arch='arm64';   sha256='f5527b7ed356767afb8a616e7b9423ef161b470e3674893e395e2a4e656deb1c' ;; 		armhf)   arch='armv6';   sha256='2c9a44ea1c289bade76770de459c437dde0bea3b44a3e7555264a63707e71470' ;; 		armv7)   arch='armv7';   sha256='0217d5704cd0be893320e686ca6bb7341991d9ed23251ac1265301994a890b6f' ;; 		ppc64le) arch='ppc64le'; sha256='1dc0fc28f368dd2d3b485f1bc7f9e5a6cb2421cf8fa94aade30fc334a362ae47' ;; 		s390x)   arch='s390x';   sha256='cbe535d6d70e5d9b6c160a6c52445eb9c90af57e12e2b5d377d1263077ae741e' ;; 		riscv64) arch='riscv64'; sha256='77cd50cd517758a5de09391d4cbda47e64caf1b67ba07413fbfbfeffed6de444' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
ENV OTEL_TRACES_EXPORTER=none
# Wed, 15 Apr 2026 20:30:47 GMT
VOLUME [/var/lib/registry]
# Wed, 15 Apr 2026 20:30:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 15 Apr 2026 20:30:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c9b070cc2b0e0766b265c2a5cfb09a8c7f75fe8cadd47ea9629e65bacb16cc`  
		Last Modified: Wed, 15 Apr 2026 20:30:55 GMT  
		Size: 290.2 KB (290153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbb7d56c8ece14a9df7df018084a367f6f952b0880a634c07cebd833f31e12b`  
		Last Modified: Wed, 15 Apr 2026 20:30:55 GMT  
		Size: 14.9 MB (14895765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0ccdbb613d063ad89a7b722b21597a9eabdcf4d35271f0a7713a7e8fea571`  
		Last Modified: Wed, 15 Apr 2026 20:30:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b9514c82ddb9ee2627d12f163b0e4fc4f72991aba4955dacfd845cadf5f603`  
		Last Modified: Wed, 15 Apr 2026 20:30:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:73882a627af94b4d13211b5f753ba8854db77bdf97934419cabeffb54d105614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 KB (280154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3570adaa19bc1e56638b03e784f79dd7af86ef99aaaec442437b8a0d8d969827`

```dockerfile
```

-	Layers:
	-	`sha256:58be04149f15e3c78295d314c2a4faa4a38af029f586050b8961fb172a3667ad`  
		Last Modified: Wed, 15 Apr 2026 20:30:55 GMT  
		Size: 265.7 KB (265736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88fbfaad15bcbecca9b0135984d3165f4938912a5befca157d2290e79e9ea5d`  
		Last Modified: Wed, 15 Apr 2026 20:30:55 GMT  
		Size: 14.4 KB (14418 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:bcf3df5fa2c662fb875bb26a72656d89e0097deb3ce23a51a221ca2acc12b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18886830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecee57321fd5a39177805029e413c51400e38aabdf05c1cf14e82c384a36982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:22:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:22:03 GMT
RUN set -eux; 	version='3.1.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='c69f2b8778c5357a77f6b41730d94d5f0b2b7cf54534040a06af5f0a70a731b2' ;; 		aarch64) arch='arm64';   sha256='f5527b7ed356767afb8a616e7b9423ef161b470e3674893e395e2a4e656deb1c' ;; 		armhf)   arch='armv6';   sha256='2c9a44ea1c289bade76770de459c437dde0bea3b44a3e7555264a63707e71470' ;; 		armv7)   arch='armv7';   sha256='0217d5704cd0be893320e686ca6bb7341991d9ed23251ac1265301994a890b6f' ;; 		ppc64le) arch='ppc64le'; sha256='1dc0fc28f368dd2d3b485f1bc7f9e5a6cb2421cf8fa94aade30fc334a362ae47' ;; 		s390x)   arch='s390x';   sha256='cbe535d6d70e5d9b6c160a6c52445eb9c90af57e12e2b5d377d1263077ae741e' ;; 		riscv64) arch='riscv64'; sha256='77cd50cd517758a5de09391d4cbda47e64caf1b67ba07413fbfbfeffed6de444' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 15 Apr 2026 20:22:03 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 15 Apr 2026 20:22:03 GMT
ENV OTEL_TRACES_EXPORTER=none
# Wed, 15 Apr 2026 20:22:03 GMT
VOLUME [/var/lib/registry]
# Wed, 15 Apr 2026 20:22:03 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 15 Apr 2026 20:22:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:22:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:22:03 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b86dcd5ed2d9c13516ee9ac0de60067820f711082d80bb186221ec31b22f6`  
		Last Modified: Wed, 15 Apr 2026 20:22:10 GMT  
		Size: 292.8 KB (292849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b078c38aa70d1267c3ad283333d6d7560ce2c35631afd41895971269b8aede`  
		Last Modified: Wed, 15 Apr 2026 20:22:11 GMT  
		Size: 14.4 MB (14393502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd362efbf0c0277065d7a85cdc42abd6de70e3a8e08baa18d6ba91a701178077`  
		Last Modified: Wed, 15 Apr 2026 20:22:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efe222c9c807ef13e6780326cb2d9fe3bb8b018a63f51cf0c12b1bb4c278775`  
		Last Modified: Wed, 15 Apr 2026 20:22:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:b647a64904ee9520f77855b55291e95eb80a097ec8ae9cd7671dd9d3f305ecf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 KB (280964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b706a42a853940983e7083d0107c97f3f58834980aac0a651b2840332fdfdc2e`

```dockerfile
```

-	Layers:
	-	`sha256:2593b7640682d2359daf4dab1115fd1b701f244563d55b5199296e117c1f67cc`  
		Last Modified: Wed, 15 Apr 2026 20:22:10 GMT  
		Size: 266.5 KB (266520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4504e5bccc28a3bbc92ec982f715222285f1cb9c7412a20dbb8d3bc7d955d4f6`  
		Last Modified: Wed, 15 Apr 2026 20:22:10 GMT  
		Size: 14.4 KB (14444 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:5638ffb2018732400cdc557e1a71fcaa8d2852e8537f0dcb36d4c02a95c4373b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18436290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4585895f0340ac7509aeb22f00de43decf80b607673ff243898be01a853903f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 21:07:30 GMT
RUN set -eux; 	version='3.1.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='c69f2b8778c5357a77f6b41730d94d5f0b2b7cf54534040a06af5f0a70a731b2' ;; 		aarch64) arch='arm64';   sha256='f5527b7ed356767afb8a616e7b9423ef161b470e3674893e395e2a4e656deb1c' ;; 		armhf)   arch='armv6';   sha256='2c9a44ea1c289bade76770de459c437dde0bea3b44a3e7555264a63707e71470' ;; 		armv7)   arch='armv7';   sha256='0217d5704cd0be893320e686ca6bb7341991d9ed23251ac1265301994a890b6f' ;; 		ppc64le) arch='ppc64le'; sha256='1dc0fc28f368dd2d3b485f1bc7f9e5a6cb2421cf8fa94aade30fc334a362ae47' ;; 		s390x)   arch='s390x';   sha256='cbe535d6d70e5d9b6c160a6c52445eb9c90af57e12e2b5d377d1263077ae741e' ;; 		riscv64) arch='riscv64'; sha256='77cd50cd517758a5de09391d4cbda47e64caf1b67ba07413fbfbfeffed6de444' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 15 Apr 2026 21:07:30 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 15 Apr 2026 21:07:31 GMT
ENV OTEL_TRACES_EXPORTER=none
# Wed, 15 Apr 2026 21:07:31 GMT
VOLUME [/var/lib/registry]
# Wed, 15 Apr 2026 21:07:31 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 15 Apr 2026 21:07:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:07:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:07:31 GMT
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
	-	`sha256:4cade354f1ce523464d53e4410066ab13054bc0f7f7f6b61c6bdab3820e81960`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 14.3 MB (14311387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bb4a94d063adb52beb225547a0ba6c3db9083b4b53b8095f04b26684e4c5a6`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b85765c8baa1e0582fde5f23baa47d49082216ba251b6dafaf4e746b5daa3e0`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:94bbd15844c18469515ab0b7240c6a6c7ae4138310b92931324b6d6e816bdce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 KB (280102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dc6237c55ac3b98cc198d4c67bd933e0ff6a353a67845bfbd58d7ca6e4a351`

```dockerfile
```

-	Layers:
	-	`sha256:c97b85e91cd831f01363bb322413a353d8468412daa3bb78eea01b0a919c8e37`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 265.7 KB (265733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95dab10b8716e4125348a762515c85bcc361e2238a4bcd7d10cd9d1161b8600c`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; riscv64

```console
$ docker pull registry@sha256:399d01da3086a1cfe669b65431a9aeb559d23c70907ff89d7d0dd025d762ff39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19196052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d07108795c4b05d32b1899916abefa6384c6d61a3c0bcd38737107e0968eb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Apr 2026 23:27:48 GMT
RUN set -eux; 	version='3.1.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='c69f2b8778c5357a77f6b41730d94d5f0b2b7cf54534040a06af5f0a70a731b2' ;; 		aarch64) arch='arm64';   sha256='f5527b7ed356767afb8a616e7b9423ef161b470e3674893e395e2a4e656deb1c' ;; 		armhf)   arch='armv6';   sha256='2c9a44ea1c289bade76770de459c437dde0bea3b44a3e7555264a63707e71470' ;; 		armv7)   arch='armv7';   sha256='0217d5704cd0be893320e686ca6bb7341991d9ed23251ac1265301994a890b6f' ;; 		ppc64le) arch='ppc64le'; sha256='1dc0fc28f368dd2d3b485f1bc7f9e5a6cb2421cf8fa94aade30fc334a362ae47' ;; 		s390x)   arch='s390x';   sha256='cbe535d6d70e5d9b6c160a6c52445eb9c90af57e12e2b5d377d1263077ae741e' ;; 		riscv64) arch='riscv64'; sha256='77cd50cd517758a5de09391d4cbda47e64caf1b67ba07413fbfbfeffed6de444' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 06 Apr 2026 23:27:48 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 06 Apr 2026 23:27:49 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 06 Apr 2026 23:27:49 GMT
VOLUME [/var/lib/registry]
# Mon, 06 Apr 2026 23:27:49 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 06 Apr 2026 23:27:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 06 Apr 2026 23:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Apr 2026 23:27:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ee3d57bba2e7c278281670ba5f5514c79cf0ab77b2a786edeed643bbdc5761`  
		Last Modified: Mon, 06 Apr 2026 23:28:58 GMT  
		Size: 15.3 MB (15313643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6c0183b45782b020ff4b675b239c2c6a15080185f8d988f5009f1b7a2c9124`  
		Last Modified: Mon, 06 Apr 2026 23:28:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d130fc919ee4ce8eaacb0a4b0af83fc727c0347fad3a16f56c078673b94cc75`  
		Last Modified: Mon, 06 Apr 2026 23:28:56 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:189347d4188a887384d821177c54662c826f5a7e21e50e07e352ca9033d85ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8c94439501dea40059e77f62c3f348b9a4c5f581ac77534229fc364fca6c4`

```dockerfile
```

-	Layers:
	-	`sha256:d5e779f84d2ce22268ff46b6f6e337d85d8d070a1da46987877eb017468491c9`  
		Last Modified: Mon, 06 Apr 2026 23:28:56 GMT  
		Size: 267.7 KB (267684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e1dab7238742df348d598d8098829a46faa973265149c30dff0fdda175f949`  
		Last Modified: Mon, 06 Apr 2026 23:28:56 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:90610ec28fe8f53272bffdf5e1cd7be96bbe6854577b57fb026677907d009959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19376711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc988d84a03a59be209cc3d90eea33d75e69465ffd7aacdbc3646b9ea914d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:41:14 GMT
RUN set -eux; 	version='3.1.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='c69f2b8778c5357a77f6b41730d94d5f0b2b7cf54534040a06af5f0a70a731b2' ;; 		aarch64) arch='arm64';   sha256='f5527b7ed356767afb8a616e7b9423ef161b470e3674893e395e2a4e656deb1c' ;; 		armhf)   arch='armv6';   sha256='2c9a44ea1c289bade76770de459c437dde0bea3b44a3e7555264a63707e71470' ;; 		armv7)   arch='armv7';   sha256='0217d5704cd0be893320e686ca6bb7341991d9ed23251ac1265301994a890b6f' ;; 		ppc64le) arch='ppc64le'; sha256='1dc0fc28f368dd2d3b485f1bc7f9e5a6cb2421cf8fa94aade30fc334a362ae47' ;; 		s390x)   arch='s390x';   sha256='cbe535d6d70e5d9b6c160a6c52445eb9c90af57e12e2b5d377d1263077ae741e' ;; 		riscv64) arch='riscv64'; sha256='77cd50cd517758a5de09391d4cbda47e64caf1b67ba07413fbfbfeffed6de444' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 15 Apr 2026 20:41:14 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 15 Apr 2026 20:41:14 GMT
ENV OTEL_TRACES_EXPORTER=none
# Wed, 15 Apr 2026 20:41:14 GMT
VOLUME [/var/lib/registry]
# Wed, 15 Apr 2026 20:41:14 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 15 Apr 2026 20:41:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:41:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:41:14 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107efaa291b5f83372c13d97ab11aebdd260da2222cd795a4f56930ce905e525`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 291.1 KB (291147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ed2ac9b04a60eb69415bcb5cc0f1a1dd9c38d7739cc439fb42e210dcd1483`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 15.4 MB (15358421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540ed722b2468503bc0a508242b89a864723e11434abc22b29b13cc1238a7077`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04f04b0a42a4b8156d317bdbd80acbd4589058f2436f75400f0cab192630f22`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:34007bb67fe7b45ea293ea6b11d5fe84296edb8d02fb48236441333b2f4730bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdda507c78449f709d08a26f0418f39212e4f66dca48c3283738f3588a16db3f`

```dockerfile
```

-	Layers:
	-	`sha256:bc4ca6abaa75ca30ee2167d2db518631d2abfa1730a2969d04329ae191103f2c`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 266.5 KB (266463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02e6f9f345869ced514962e24fb7ba1ee0058347b0b0820b2731667a44b03d3`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json
