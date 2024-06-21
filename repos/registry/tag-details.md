<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-alpha.1`](#registry300-alpha1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:79b29591e1601a73f03fcd413e655b72b9abfae5a23f1ad2e883d4942fbb4351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:ce1ffcfadba406bcca40445dc1c8e60a38565fe35504ea0f77d753ab72340d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9475412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7893587f384c7e8a47b6d3afca915b7db83f3b19e34fc6e02fbeaa1b3c94020f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73926982f2889513cbc08351601bf7c988fdca288aac193ad769ec8f792782ba`  
		Last Modified: Fri, 21 Jun 2024 04:57:38 GMT  
		Size: 294.0 KB (294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c400d8448401ced06a76b09a49e245250ceb40277db557153b19efe8f7ac40a`  
		Last Modified: Fri, 21 Jun 2024 04:57:57 GMT  
		Size: 6.0 MB (6024108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d3e733d8ec50b4b7e95b9d3ba86cacd63b46a69d7de92b09279a7a948490d`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182d8c165e052f46143c4cd0423deaba4d4fc1867f5aed48fbd09654f125c5b7`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:5c6b6bc6dc49de2ad21ad3c59bf8270061d3127ad9c5ba3da42b75ef1d968ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba4642827c63c3d30076176960dc4f2488cf06c1b9d8a1973bbad60d00c24d`

```dockerfile
```

-	Layers:
	-	`sha256:0adb6cf3fde0cf7366f0367f31e3b414cbce931e992f82a7aaf9b42b4542d81b`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:d3fc4294cbac7410858efd59bd02f605e7ea7104e108be59752c0ec5bf937850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9219382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b930480d05c46f68bee2cd92fae8fcb947821467aa73ce1eb575d35282dec6bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4c88704b1aa2490c90156fed455d61b297200b334e12270d63e0de8edafd08`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d673617c406522825a89c05c3bd98422334b930e9873174463ada7d423e85`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e31606a4375df78c4e3ac7ede99b16a1c088174f8280225feb656d5e54f3b5`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ebcd1fe14d7a603c6e72b18dce1d81e55932652d0b9f439a392726f36245d`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:679a50937fc268b6f6b081b28ab1ab03964f22dd2c9466744d9a73eeb30d5369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 KB (189199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ad0759fbbab0e5f70c003e10371f7cbab59c1bf9f3beb44b4aecdb395cdcd5`

```dockerfile
```

-	Layers:
	-	`sha256:e95dffa23eebbc96dee0dbdeb5747728dfc536549484ee3f3d3c0d24faf44a9e`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 175.3 KB (175314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51c3139a7205642f422d64725325c5567a5f4e9e5e5bf085b1a7bd1d6458d59`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4c0302a993b05bd8151a08735b0918b8903b82d3a65e14023e3a61eb5b11a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9459193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bd730847e7eb75ccdc376f170edd44565090b2dcc628de3f2dabd454a25ddf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4b076db674ffa39d1802f24493e23fd4d26e149ac3dc3c7e64cfeedf804941`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 295.9 KB (295928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44632a7c67902d31dff5feb72ed4613ad1599fcfb854ead2d78abec33497362f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e959b0d8fe39d51c902820d1b9263fd96e1d94c3992fb2cd1776e7b2333d2`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cf2a2c24d3b498f205b5c36a1154f24e60314716cfac27b2c88cde6400f1f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:1a5ffd347d918888c907a897860b5b56153418fad581420a39370c124bd9fcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 KB (189436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44ae0ebfe8f510731a11318090d1f7e8d3d7058804757c4bca9a4b807967d2`

```dockerfile
```

-	Layers:
	-	`sha256:b1474abbed9bb94238325624891b0ac3a1a317158e047b10c48e8e31d9473a07`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 175.3 KB (175334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd2979c93c33b6c0aff78b2109a3d0f863952ddf4051042469c9ad4ba50581d`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 14.1 KB (14102 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:34b23db1730dc6d1789a2b1008f63f935342029d09b04151ab15e57e0180d333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9343073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dbca443518974c4b51588a3218e1752518620993bab5857c54eb37cf649f9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05e1ee509fa227e192e4093cc795b1da364e20113b227af25a6ba5b44f6c7f`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69344abf7da1ba7c0a2428776f4e5c90ed5360eca15f3e1d3fc71009cce3a2`  
		Last Modified: Fri, 21 Jun 2024 02:55:21 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a8d79d11f5c46636c8d091dcc04d0657f6a56b649c9e3f1bdd86c1aaaa685`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81d7fc89a2d1d62b3852a262103ac050961ba68bab11e6f44c903f9d64539a`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:a2aaa41f80e13ccb0c9bb3daf24924fb4386db87b15b0682d862786ace663c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 KB (187200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd018658d1a1175a6ac1588ca1d12266514afa77c28de3c8b8d0cc8c9aec5cbd`

```dockerfile
```

-	Layers:
	-	`sha256:981b8bed9f3446bc21dfa71ccaf461123ed144207efbcc615923796c37d7f73d`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 173.4 KB (173358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd7591901a1a1e922a8ab2e812e2feb3488a71b7026d4221de6d94f7f059b56`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 13.8 KB (13842 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:073d565951025666ab3cf8cb8a7e3b87f3edd831cc810dcb31b5f54ed9345831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9682990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d284c81a1e4b1a06e770a9b301d90d12b65bdc0e494bf8a020705cee5e6e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:066d299d4861b197660e02b5eb126c42f2a11e586f49c463174acf5454e9244b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:784fb6b11ccf355c65e296bcf7ef3623ff36c33ac16292b79440c32ec3699700`  
		Last Modified: Thu, 20 Jun 2024 17:43:27 GMT  
		Size: 3.2 MB (3228474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a426eb93b7b93c73794517c84ef71d7dcc4719e45e3655858f9683fcb0633`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae11a7490fe3ced24ccdbc59f281f831e48ddbb146bb7fa40fafbc1f3bfdac`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9598ab3a7b8dd012bdec4ff075f9923d716b6689266552d93a0fc3e0f7a540ad`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5653a2b64ae246042e6da1455594cad84e0f66e5791f41a8977b901969bcc8`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:d8ec038648b94d846f00c0854cb0585aca2e0f8a27a4d3b8e5495fd32b8f1ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 KB (187126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81185b8c3188e756c7114cc1de3a804ee71982ba148042bf21fcdde42a141033`

```dockerfile
```

-	Layers:
	-	`sha256:9f9a2b5f8d3d64fde595808b735b6608f04a83bc682d3e66835713dcc62c59a3`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 173.3 KB (173324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca581e0d26d0109b01af03a306769d95fc65edaec5b1bcc08d6edd0dc005591`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:79b29591e1601a73f03fcd413e655b72b9abfae5a23f1ad2e883d4942fbb4351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `registry:2.8` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:ce1ffcfadba406bcca40445dc1c8e60a38565fe35504ea0f77d753ab72340d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9475412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7893587f384c7e8a47b6d3afca915b7db83f3b19e34fc6e02fbeaa1b3c94020f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73926982f2889513cbc08351601bf7c988fdca288aac193ad769ec8f792782ba`  
		Last Modified: Fri, 21 Jun 2024 04:57:38 GMT  
		Size: 294.0 KB (294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c400d8448401ced06a76b09a49e245250ceb40277db557153b19efe8f7ac40a`  
		Last Modified: Fri, 21 Jun 2024 04:57:57 GMT  
		Size: 6.0 MB (6024108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d3e733d8ec50b4b7e95b9d3ba86cacd63b46a69d7de92b09279a7a948490d`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182d8c165e052f46143c4cd0423deaba4d4fc1867f5aed48fbd09654f125c5b7`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:5c6b6bc6dc49de2ad21ad3c59bf8270061d3127ad9c5ba3da42b75ef1d968ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba4642827c63c3d30076176960dc4f2488cf06c1b9d8a1973bbad60d00c24d`

```dockerfile
```

-	Layers:
	-	`sha256:0adb6cf3fde0cf7366f0367f31e3b414cbce931e992f82a7aaf9b42b4542d81b`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:d3fc4294cbac7410858efd59bd02f605e7ea7104e108be59752c0ec5bf937850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9219382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b930480d05c46f68bee2cd92fae8fcb947821467aa73ce1eb575d35282dec6bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4c88704b1aa2490c90156fed455d61b297200b334e12270d63e0de8edafd08`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d673617c406522825a89c05c3bd98422334b930e9873174463ada7d423e85`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e31606a4375df78c4e3ac7ede99b16a1c088174f8280225feb656d5e54f3b5`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ebcd1fe14d7a603c6e72b18dce1d81e55932652d0b9f439a392726f36245d`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:679a50937fc268b6f6b081b28ab1ab03964f22dd2c9466744d9a73eeb30d5369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 KB (189199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ad0759fbbab0e5f70c003e10371f7cbab59c1bf9f3beb44b4aecdb395cdcd5`

```dockerfile
```

-	Layers:
	-	`sha256:e95dffa23eebbc96dee0dbdeb5747728dfc536549484ee3f3d3c0d24faf44a9e`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 175.3 KB (175314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51c3139a7205642f422d64725325c5567a5f4e9e5e5bf085b1a7bd1d6458d59`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4c0302a993b05bd8151a08735b0918b8903b82d3a65e14023e3a61eb5b11a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9459193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bd730847e7eb75ccdc376f170edd44565090b2dcc628de3f2dabd454a25ddf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4b076db674ffa39d1802f24493e23fd4d26e149ac3dc3c7e64cfeedf804941`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 295.9 KB (295928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44632a7c67902d31dff5feb72ed4613ad1599fcfb854ead2d78abec33497362f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e959b0d8fe39d51c902820d1b9263fd96e1d94c3992fb2cd1776e7b2333d2`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cf2a2c24d3b498f205b5c36a1154f24e60314716cfac27b2c88cde6400f1f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:1a5ffd347d918888c907a897860b5b56153418fad581420a39370c124bd9fcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 KB (189436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44ae0ebfe8f510731a11318090d1f7e8d3d7058804757c4bca9a4b807967d2`

```dockerfile
```

-	Layers:
	-	`sha256:b1474abbed9bb94238325624891b0ac3a1a317158e047b10c48e8e31d9473a07`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 175.3 KB (175334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd2979c93c33b6c0aff78b2109a3d0f863952ddf4051042469c9ad4ba50581d`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 14.1 KB (14102 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:34b23db1730dc6d1789a2b1008f63f935342029d09b04151ab15e57e0180d333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9343073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dbca443518974c4b51588a3218e1752518620993bab5857c54eb37cf649f9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05e1ee509fa227e192e4093cc795b1da364e20113b227af25a6ba5b44f6c7f`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69344abf7da1ba7c0a2428776f4e5c90ed5360eca15f3e1d3fc71009cce3a2`  
		Last Modified: Fri, 21 Jun 2024 02:55:21 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a8d79d11f5c46636c8d091dcc04d0657f6a56b649c9e3f1bdd86c1aaaa685`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81d7fc89a2d1d62b3852a262103ac050961ba68bab11e6f44c903f9d64539a`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:a2aaa41f80e13ccb0c9bb3daf24924fb4386db87b15b0682d862786ace663c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 KB (187200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd018658d1a1175a6ac1588ca1d12266514afa77c28de3c8b8d0cc8c9aec5cbd`

```dockerfile
```

-	Layers:
	-	`sha256:981b8bed9f3446bc21dfa71ccaf461123ed144207efbcc615923796c37d7f73d`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 173.4 KB (173358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd7591901a1a1e922a8ab2e812e2feb3488a71b7026d4221de6d94f7f059b56`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 13.8 KB (13842 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:073d565951025666ab3cf8cb8a7e3b87f3edd831cc810dcb31b5f54ed9345831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9682990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d284c81a1e4b1a06e770a9b301d90d12b65bdc0e494bf8a020705cee5e6e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:066d299d4861b197660e02b5eb126c42f2a11e586f49c463174acf5454e9244b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:784fb6b11ccf355c65e296bcf7ef3623ff36c33ac16292b79440c32ec3699700`  
		Last Modified: Thu, 20 Jun 2024 17:43:27 GMT  
		Size: 3.2 MB (3228474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a426eb93b7b93c73794517c84ef71d7dcc4719e45e3655858f9683fcb0633`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae11a7490fe3ced24ccdbc59f281f831e48ddbb146bb7fa40fafbc1f3bfdac`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9598ab3a7b8dd012bdec4ff075f9923d716b6689266552d93a0fc3e0f7a540ad`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5653a2b64ae246042e6da1455594cad84e0f66e5791f41a8977b901969bcc8`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:d8ec038648b94d846f00c0854cb0585aca2e0f8a27a4d3b8e5495fd32b8f1ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 KB (187126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81185b8c3188e756c7114cc1de3a804ee71982ba148042bf21fcdde42a141033`

```dockerfile
```

-	Layers:
	-	`sha256:9f9a2b5f8d3d64fde595808b735b6608f04a83bc682d3e66835713dcc62c59a3`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 173.3 KB (173324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca581e0d26d0109b01af03a306769d95fc65edaec5b1bcc08d6edd0dc005591`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:79b29591e1601a73f03fcd413e655b72b9abfae5a23f1ad2e883d4942fbb4351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `registry:2.8.3` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:ce1ffcfadba406bcca40445dc1c8e60a38565fe35504ea0f77d753ab72340d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9475412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7893587f384c7e8a47b6d3afca915b7db83f3b19e34fc6e02fbeaa1b3c94020f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73926982f2889513cbc08351601bf7c988fdca288aac193ad769ec8f792782ba`  
		Last Modified: Fri, 21 Jun 2024 04:57:38 GMT  
		Size: 294.0 KB (294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c400d8448401ced06a76b09a49e245250ceb40277db557153b19efe8f7ac40a`  
		Last Modified: Fri, 21 Jun 2024 04:57:57 GMT  
		Size: 6.0 MB (6024108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d3e733d8ec50b4b7e95b9d3ba86cacd63b46a69d7de92b09279a7a948490d`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182d8c165e052f46143c4cd0423deaba4d4fc1867f5aed48fbd09654f125c5b7`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:5c6b6bc6dc49de2ad21ad3c59bf8270061d3127ad9c5ba3da42b75ef1d968ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba4642827c63c3d30076176960dc4f2488cf06c1b9d8a1973bbad60d00c24d`

```dockerfile
```

-	Layers:
	-	`sha256:0adb6cf3fde0cf7366f0367f31e3b414cbce931e992f82a7aaf9b42b4542d81b`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:d3fc4294cbac7410858efd59bd02f605e7ea7104e108be59752c0ec5bf937850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9219382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b930480d05c46f68bee2cd92fae8fcb947821467aa73ce1eb575d35282dec6bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4c88704b1aa2490c90156fed455d61b297200b334e12270d63e0de8edafd08`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d673617c406522825a89c05c3bd98422334b930e9873174463ada7d423e85`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e31606a4375df78c4e3ac7ede99b16a1c088174f8280225feb656d5e54f3b5`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ebcd1fe14d7a603c6e72b18dce1d81e55932652d0b9f439a392726f36245d`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:679a50937fc268b6f6b081b28ab1ab03964f22dd2c9466744d9a73eeb30d5369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 KB (189199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ad0759fbbab0e5f70c003e10371f7cbab59c1bf9f3beb44b4aecdb395cdcd5`

```dockerfile
```

-	Layers:
	-	`sha256:e95dffa23eebbc96dee0dbdeb5747728dfc536549484ee3f3d3c0d24faf44a9e`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 175.3 KB (175314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51c3139a7205642f422d64725325c5567a5f4e9e5e5bf085b1a7bd1d6458d59`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4c0302a993b05bd8151a08735b0918b8903b82d3a65e14023e3a61eb5b11a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9459193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bd730847e7eb75ccdc376f170edd44565090b2dcc628de3f2dabd454a25ddf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4b076db674ffa39d1802f24493e23fd4d26e149ac3dc3c7e64cfeedf804941`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 295.9 KB (295928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44632a7c67902d31dff5feb72ed4613ad1599fcfb854ead2d78abec33497362f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e959b0d8fe39d51c902820d1b9263fd96e1d94c3992fb2cd1776e7b2333d2`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cf2a2c24d3b498f205b5c36a1154f24e60314716cfac27b2c88cde6400f1f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:1a5ffd347d918888c907a897860b5b56153418fad581420a39370c124bd9fcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 KB (189436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44ae0ebfe8f510731a11318090d1f7e8d3d7058804757c4bca9a4b807967d2`

```dockerfile
```

-	Layers:
	-	`sha256:b1474abbed9bb94238325624891b0ac3a1a317158e047b10c48e8e31d9473a07`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 175.3 KB (175334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd2979c93c33b6c0aff78b2109a3d0f863952ddf4051042469c9ad4ba50581d`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 14.1 KB (14102 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:34b23db1730dc6d1789a2b1008f63f935342029d09b04151ab15e57e0180d333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9343073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dbca443518974c4b51588a3218e1752518620993bab5857c54eb37cf649f9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05e1ee509fa227e192e4093cc795b1da364e20113b227af25a6ba5b44f6c7f`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69344abf7da1ba7c0a2428776f4e5c90ed5360eca15f3e1d3fc71009cce3a2`  
		Last Modified: Fri, 21 Jun 2024 02:55:21 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a8d79d11f5c46636c8d091dcc04d0657f6a56b649c9e3f1bdd86c1aaaa685`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81d7fc89a2d1d62b3852a262103ac050961ba68bab11e6f44c903f9d64539a`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:a2aaa41f80e13ccb0c9bb3daf24924fb4386db87b15b0682d862786ace663c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 KB (187200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd018658d1a1175a6ac1588ca1d12266514afa77c28de3c8b8d0cc8c9aec5cbd`

```dockerfile
```

-	Layers:
	-	`sha256:981b8bed9f3446bc21dfa71ccaf461123ed144207efbcc615923796c37d7f73d`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 173.4 KB (173358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd7591901a1a1e922a8ab2e812e2feb3488a71b7026d4221de6d94f7f059b56`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 13.8 KB (13842 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:073d565951025666ab3cf8cb8a7e3b87f3edd831cc810dcb31b5f54ed9345831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9682990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d284c81a1e4b1a06e770a9b301d90d12b65bdc0e494bf8a020705cee5e6e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:066d299d4861b197660e02b5eb126c42f2a11e586f49c463174acf5454e9244b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:784fb6b11ccf355c65e296bcf7ef3623ff36c33ac16292b79440c32ec3699700`  
		Last Modified: Thu, 20 Jun 2024 17:43:27 GMT  
		Size: 3.2 MB (3228474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a426eb93b7b93c73794517c84ef71d7dcc4719e45e3655858f9683fcb0633`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae11a7490fe3ced24ccdbc59f281f831e48ddbb146bb7fa40fafbc1f3bfdac`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9598ab3a7b8dd012bdec4ff075f9923d716b6689266552d93a0fc3e0f7a540ad`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5653a2b64ae246042e6da1455594cad84e0f66e5791f41a8977b901969bcc8`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:d8ec038648b94d846f00c0854cb0585aca2e0f8a27a4d3b8e5495fd32b8f1ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 KB (187126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81185b8c3188e756c7114cc1de3a804ee71982ba148042bf21fcdde42a141033`

```dockerfile
```

-	Layers:
	-	`sha256:9f9a2b5f8d3d64fde595808b735b6608f04a83bc682d3e66835713dcc62c59a3`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 173.3 KB (173324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca581e0d26d0109b01af03a306769d95fc65edaec5b1bcc08d6edd0dc005591`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-alpha.1`

```console
$ docker pull registry@sha256:5f6ae37d27fb3a137794e526ee826bb8d01c6162b696a0a0afca094b3f0b5b18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `registry:3.0.0-alpha.1` - linux; amd64

```console
$ docker pull registry@sha256:f81e277b902d07c4958ea3c7197e60d5165f788f1122f4da15cf750915f8c233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14227375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8bd2463b7aa3dd5f16c2273acab73b4845c8e500eecc96852e61cf8b61d853`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c6d1270bb225221a153af79aff12dc32e789f4d92422539d1be94ae588fcba`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 293.4 KB (293367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6fdd5c51aea5598edca216ed6012cbc7d6effb1672a55180965a4b87cc747a`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 10.5 MB (10519529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d02916a0c0722bc525fef2008e2fa182929af35f8fd9529b425b4d337f2714`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5379317961932fb8b1d41f78289cef5a0eacf4fbc923da1412d54cafc283e573`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:0d73f5ce8d6f85be7ad50b20fd730fc5381d580ad9c67b47124dcbd9199b7cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 KB (243985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075b66ac307c215fc1fa8949a55b6c034c095c5f72a03fd7c8393531e23f8965`

```dockerfile
```

-	Layers:
	-	`sha256:20b93925ee23a11f66f706ed8d7f4eea8bd063ce25453b2b542edd33378d45d5`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 231.0 KB (231038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fbcc779301a238e3c0aca368edd8cbd513d3ea367ca274eb41ecec5c7b09`  
		Last Modified: Thu, 20 Jun 2024 20:55:58 GMT  
		Size: 12.9 KB (12947 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:f02867a52e2c02de7a52ce542fc6bba2487682ae716a24373be98e02a988821b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0344417aa70b3165e03b70b23bce4b686bc55535ecf8ba845e7f32c3b9472b44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73926982f2889513cbc08351601bf7c988fdca288aac193ad769ec8f792782ba`  
		Last Modified: Fri, 21 Jun 2024 04:57:38 GMT  
		Size: 294.0 KB (294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b9757f676e1de5f590df8051533f2c01e7aafb94d722c7fcd76590fbdc11b`  
		Last Modified: Fri, 21 Jun 2024 04:57:39 GMT  
		Size: 10.0 MB (9965004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2524b6640c8c6899f6662c4712a6602c0fe20c658f872b15603e2f4981efafd4`  
		Last Modified: Fri, 21 Jun 2024 04:57:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeab14df2fb084398f441e91cceafa284dfc370588bb2f6062c3772fdfca00a`  
		Last Modified: Fri, 21 Jun 2024 04:57:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:9ceff7f32097e38af741a65d8c7d51ac60afb0bdd55717f98d737c476f94afe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3958d51fb9fc8c8aae92a80426e4c43307e402d6099f93ac7687ec60a770f5`

```dockerfile
```

-	Layers:
	-	`sha256:4388eb2ba62be15b6af6a4566ae63562cae32800ccb5667943f56f6d268c4c83`  
		Last Modified: Fri, 21 Jun 2024 04:57:38 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:9ef6f7da33c9b8bb308cdbbc1baf4e3c9fdbbc979970a30bfd84c2266d2bd110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13156716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e64ab83b24348d069036cee314c17fef1c9d3949429f76e7e5e4e3f8820a6d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4c88704b1aa2490c90156fed455d61b297200b334e12270d63e0de8edafd08`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7d6be1ea00e2aa14e3c7d9ea7281184803e90709489e2517c2fc2330a0cb60`  
		Last Modified: Fri, 21 Jun 2024 04:46:47 GMT  
		Size: 10.0 MB (9954543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcca4ebe97e9e9459ff99217b84f1d742993a50a6ddb71a20b1783dd9247f86`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a080b1277a889cb6fce9ea8b945ac5abea503bb516f5efb72b8efa36f1ae3804`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:7d8a6b1a29c5a2c26fdfab0ca012a750bed90473478314a0fa54881f37bac8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 KB (244053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58639d086e76f8d9b4dbfcd5d7eff49d9dd87cc3eb9ffb7c8477888c81a280cb`

```dockerfile
```

-	Layers:
	-	`sha256:69380f6b860da6bfb623b13e793da15db6480bef21dd375025a05ef7974cd330`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 231.1 KB (231050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39af5e4fa4a5ca34cdedac90d1f295b380e46404a9f99951e8bcb186bf8d4878`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 13.0 KB (13003 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4515de4bfc81fee3cb2b31943efb3d2c8b0df5235ee335029856c46153146f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13363959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f156cbda94fddcde8c891145587cca975b070242b5484e2d77fa9ce4019dec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4b076db674ffa39d1802f24493e23fd4d26e149ac3dc3c7e64cfeedf804941`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 295.9 KB (295928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f5a17ab475008db876d6315ca85208d82bae8a418271d88d57e541d5162879`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 9.7 MB (9729498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fcc8ad25a9ad391e0bfb586128a3e700a039adf291aff19c5255373c0e66a9`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d41a3609df63424545d26351b4321dd4793a8497a77657400922337de92f567`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:6a4dcfee9c4e7314585c578309b783e3dd3e8fa31d8d93fe18b0c5abe1ef3e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 KB (244266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bd09e5e06b6247e69f50c2a8c04ea7114671c814df2c95230b96717b214832`

```dockerfile
```

-	Layers:
	-	`sha256:c046b7fa3391195efa6f45fa7145d9040a7f78db4bc4b5704305f5b2c09972bb`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 231.1 KB (231058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e658414f31af2b32bdb95f670e15b32d491e5f5a47bca86324f93dce8102307`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 13.2 KB (13208 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; ppc64le

```console
$ docker pull registry@sha256:2201076e6497c33ea001e68653f3127d5ffca6e6cb221a4987dfeac3896b67a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13128421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0428b65e43f068007b989e016c5ed449c470d906f9af9b6b92391ff492fd91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05e1ee509fa227e192e4093cc795b1da364e20113b227af25a6ba5b44f6c7f`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea250429436a25f14a28030268a77ac2c21241bee78bf44eae42fe5d6f84b28e`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 9.5 MB (9474563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb67ddb3d680176e0b0d68800057e790f02948f9eb96af10e8995b21091aaca`  
		Last Modified: Fri, 21 Jun 2024 02:54:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e008973831e319dbc459ec5109368c373b872861a49be2ce4dd264fbaf904e4e`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:b3c1415a685999a3d80badc20b46ebb44b66eda25cb81f50128fe9766b327e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 KB (242066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3281341403ba45c49c539fd54bc8b516fab0c9d5a61ca45fcbda1dc3b4a9fe2`

```dockerfile
```

-	Layers:
	-	`sha256:2c8940f8b6c52a274e0009fc3b90a37c5926c10d294ce1c6832d1a94a5e725c5`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 229.1 KB (229100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5f81e23d83f62feffd4bc79122dce510ab3cde01e35c515766ac211b0cd165`  
		Last Modified: Fri, 21 Jun 2024 02:54:55 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-alpha.1` - linux; s390x

```console
$ docker pull registry@sha256:debf3acc1f75a2d2b6236e60e5dc41e75427b660d16223fecb72d88a694b0aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13618129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc14dcec60cbb93e12767e9133b824a09f6c401684ddbfe32b6b52fbfdcbc693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Tue, 19 Dec 2023 16:37:37 GMT
ADD file:066d299d4861b197660e02b5eb126c42f2a11e586f49c463174acf5454e9244b in / 
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 16:37:37 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 19 Dec 2023 16:37:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Dec 2023 16:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 16:37:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:784fb6b11ccf355c65e296bcf7ef3623ff36c33ac16292b79440c32ec3699700`  
		Last Modified: Thu, 20 Jun 2024 17:43:27 GMT  
		Size: 3.2 MB (3228474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a426eb93b7b93c73794517c84ef71d7dcc4719e45e3655858f9683fcb0633`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c29ef2e1654367967212759798f80d197a7d73e8275710f3e09daa1f2bf445b`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 10.1 MB (10095187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9b00be44f38bea708b2031f14e5f819b27bb5a4f9158ed88896bd152acb09`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420109cd17f121ce53c8590ea311e0cd79b30973b07aca43083afa34cbb28108`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-alpha.1` - unknown; unknown

```console
$ docker pull registry@sha256:f6b5662fde021034d6707bfdf3d2da75031c42c2d0c7496195a3db45abff3cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 KB (242015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fad20d4291b4b65f0184a85818aebc074f84cc30b9a0223c3d23e992421d8fd`

```dockerfile
```

-	Layers:
	-	`sha256:70b3652dfe6d64042d0ee7015bfff27f617615057eb4df12c44208db74fc46b4`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 229.1 KB (229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d9ec661055ae858c681a42b8c038da54a2096c220913aef0b61134f1043b1f`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 12.9 KB (12947 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:79b29591e1601a73f03fcd413e655b72b9abfae5a23f1ad2e883d4942fbb4351
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:97479ff6bb309b6f667458d9f3391dbd1ba87a3d5c4a1b486570ae87e8261a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3edb1d5eb6923955548ab7f391e5cc2f04e929c3d32447a7480d8b7a87a0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490907166411a51582f8f9bb5efa7a4f3dffeba3cfeb432a1bb86bcf3e40c77`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 293.4 KB (293373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f2b8a18ff7d043b424e13bb9a942587ea819d18ba3823aff5375b92115815`  
		Last Modified: Thu, 20 Jun 2024 20:56:03 GMT  
		Size: 6.4 MB (6403785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41963883ad33a376d1b2d0ad4b2bdc45a6fbe9531e95324ce476b769e82c52`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02dd2076d659eaac7ce8995ca97151e70196bf3c7ffa6fe3f5f59aa0da96eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:63c6d9ec427e37346c35f2a0f2f1474e4a8d23e49e514f5e7b8df1114182a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 KB (189080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1fd022de1de96143891948bb6ff8698ecbf9e9a2e851bb792e4ed3437e358a`

```dockerfile
```

-	Layers:
	-	`sha256:945dc0138af5f8fd304e0a62b2728da575027980125b7f0854738ab8caa67d99`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 175.3 KB (175278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daff06b9bac2985d18acc823c4ec30bb389a6afe1de0dc80842f0c27dfd1dfff`  
		Last Modified: Thu, 20 Jun 2024 20:56:02 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:ce1ffcfadba406bcca40445dc1c8e60a38565fe35504ea0f77d753ab72340d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9475412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7893587f384c7e8a47b6d3afca915b7db83f3b19e34fc6e02fbeaa1b3c94020f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73926982f2889513cbc08351601bf7c988fdca288aac193ad769ec8f792782ba`  
		Last Modified: Fri, 21 Jun 2024 04:57:38 GMT  
		Size: 294.0 KB (294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c400d8448401ced06a76b09a49e245250ceb40277db557153b19efe8f7ac40a`  
		Last Modified: Fri, 21 Jun 2024 04:57:57 GMT  
		Size: 6.0 MB (6024108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d3e733d8ec50b4b7e95b9d3ba86cacd63b46a69d7de92b09279a7a948490d`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182d8c165e052f46143c4cd0423deaba4d4fc1867f5aed48fbd09654f125c5b7`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:5c6b6bc6dc49de2ad21ad3c59bf8270061d3127ad9c5ba3da42b75ef1d968ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba4642827c63c3d30076176960dc4f2488cf06c1b9d8a1973bbad60d00c24d`

```dockerfile
```

-	Layers:
	-	`sha256:0adb6cf3fde0cf7366f0367f31e3b414cbce931e992f82a7aaf9b42b4542d81b`  
		Last Modified: Fri, 21 Jun 2024 04:57:56 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:d3fc4294cbac7410858efd59bd02f605e7ea7104e108be59752c0ec5bf937850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9219382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b930480d05c46f68bee2cd92fae8fcb947821467aa73ce1eb575d35282dec6bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4c88704b1aa2490c90156fed455d61b297200b334e12270d63e0de8edafd08`  
		Last Modified: Fri, 21 Jun 2024 04:46:46 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d673617c406522825a89c05c3bd98422334b930e9873174463ada7d423e85`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e31606a4375df78c4e3ac7ede99b16a1c088174f8280225feb656d5e54f3b5`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ebcd1fe14d7a603c6e72b18dce1d81e55932652d0b9f439a392726f36245d`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:679a50937fc268b6f6b081b28ab1ab03964f22dd2c9466744d9a73eeb30d5369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 KB (189199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ad0759fbbab0e5f70c003e10371f7cbab59c1bf9f3beb44b4aecdb395cdcd5`

```dockerfile
```

-	Layers:
	-	`sha256:e95dffa23eebbc96dee0dbdeb5747728dfc536549484ee3f3d3c0d24faf44a9e`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 175.3 KB (175314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51c3139a7205642f422d64725325c5567a5f4e9e5e5bf085b1a7bd1d6458d59`  
		Last Modified: Fri, 21 Jun 2024 04:47:07 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:4c0302a993b05bd8151a08735b0918b8903b82d3a65e14023e3a61eb5b11a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9459193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bd730847e7eb75ccdc376f170edd44565090b2dcc628de3f2dabd454a25ddf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4b076db674ffa39d1802f24493e23fd4d26e149ac3dc3c7e64cfeedf804941`  
		Last Modified: Fri, 21 Jun 2024 06:27:13 GMT  
		Size: 295.9 KB (295928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44632a7c67902d31dff5feb72ed4613ad1599fcfb854ead2d78abec33497362f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e959b0d8fe39d51c902820d1b9263fd96e1d94c3992fb2cd1776e7b2333d2`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cf2a2c24d3b498f205b5c36a1154f24e60314716cfac27b2c88cde6400f1f`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1a5ffd347d918888c907a897860b5b56153418fad581420a39370c124bd9fcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 KB (189436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44ae0ebfe8f510731a11318090d1f7e8d3d7058804757c4bca9a4b807967d2`

```dockerfile
```

-	Layers:
	-	`sha256:b1474abbed9bb94238325624891b0ac3a1a317158e047b10c48e8e31d9473a07`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 175.3 KB (175334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd2979c93c33b6c0aff78b2109a3d0f863952ddf4051042469c9ad4ba50581d`  
		Last Modified: Fri, 21 Jun 2024 06:27:35 GMT  
		Size: 14.1 KB (14102 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:34b23db1730dc6d1789a2b1008f63f935342029d09b04151ab15e57e0180d333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9343073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dbca443518974c4b51588a3218e1752518620993bab5857c54eb37cf649f9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05e1ee509fa227e192e4093cc795b1da364e20113b227af25a6ba5b44f6c7f`  
		Last Modified: Fri, 21 Jun 2024 02:54:56 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69344abf7da1ba7c0a2428776f4e5c90ed5360eca15f3e1d3fc71009cce3a2`  
		Last Modified: Fri, 21 Jun 2024 02:55:21 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a8d79d11f5c46636c8d091dcc04d0657f6a56b649c9e3f1bdd86c1aaaa685`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81d7fc89a2d1d62b3852a262103ac050961ba68bab11e6f44c903f9d64539a`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:a2aaa41f80e13ccb0c9bb3daf24924fb4386db87b15b0682d862786ace663c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 KB (187200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd018658d1a1175a6ac1588ca1d12266514afa77c28de3c8b8d0cc8c9aec5cbd`

```dockerfile
```

-	Layers:
	-	`sha256:981b8bed9f3446bc21dfa71ccaf461123ed144207efbcc615923796c37d7f73d`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 173.4 KB (173358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd7591901a1a1e922a8ab2e812e2feb3488a71b7026d4221de6d94f7f059b56`  
		Last Modified: Fri, 21 Jun 2024 02:55:20 GMT  
		Size: 13.8 KB (13842 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:073d565951025666ab3cf8cb8a7e3b87f3edd831cc810dcb31b5f54ed9345831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9682990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d284c81a1e4b1a06e770a9b301d90d12b65bdc0e494bf8a020705cee5e6e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:066d299d4861b197660e02b5eb126c42f2a11e586f49c463174acf5454e9244b in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:784fb6b11ccf355c65e296bcf7ef3623ff36c33ac16292b79440c32ec3699700`  
		Last Modified: Thu, 20 Jun 2024 17:43:27 GMT  
		Size: 3.2 MB (3228474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a426eb93b7b93c73794517c84ef71d7dcc4719e45e3655858f9683fcb0633`  
		Last Modified: Fri, 21 Jun 2024 05:39:43 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae11a7490fe3ced24ccdbc59f281f831e48ddbb146bb7fa40fafbc1f3bfdac`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9598ab3a7b8dd012bdec4ff075f9923d716b6689266552d93a0fc3e0f7a540ad`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5653a2b64ae246042e6da1455594cad84e0f66e5791f41a8977b901969bcc8`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:d8ec038648b94d846f00c0854cb0585aca2e0f8a27a4d3b8e5495fd32b8f1ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 KB (187126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81185b8c3188e756c7114cc1de3a804ee71982ba148042bf21fcdde42a141033`

```dockerfile
```

-	Layers:
	-	`sha256:9f9a2b5f8d3d64fde595808b735b6608f04a83bc682d3e66835713dcc62c59a3`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 173.3 KB (173324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca581e0d26d0109b01af03a306769d95fc65edaec5b1bcc08d6edd0dc005591`  
		Last Modified: Fri, 21 Jun 2024 05:40:23 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json
