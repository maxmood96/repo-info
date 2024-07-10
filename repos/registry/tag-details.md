<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-beta.1`](#registry300-beta1)
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

## `registry:3.0.0-beta.1`

```console
$ docker pull registry@sha256:3bf4e23aa3d15447e596e3dac6368a569d43afb5e970929879344eb7721904ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.0.0-beta.1` - linux; amd64

```console
$ docker pull registry@sha256:2b7e16320a3e11e9de2ba6c2ce143dc5898b0b26c650667e7d5999164023f36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b1a4c789497d1b6f38c600b93882cfa8fed41b02360908f0bdf8ed2de8c927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fe5aaaf843add1d2b3b255f5d02b89222a379660b863a82d69526c33c78694`  
		Last Modified: Wed, 10 Jul 2024 16:57:53 GMT  
		Size: 290.9 KB (290933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a5e30ee79c505ade6617ec394edd56f436e0b5def1d5638fc7215a1fe60311`  
		Last Modified: Wed, 10 Jul 2024 16:57:54 GMT  
		Size: 11.0 MB (10995724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24aa31cfc71bf593195ef89d6070536f63b764e325ca5054b66cb9d955653469`  
		Last Modified: Wed, 10 Jul 2024 16:57:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911e692a8360e40e5c84604dee5d4be75458579bf47d90534de368d34a2ca1f1`  
		Last Modified: Wed, 10 Jul 2024 16:57:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:58be58deef9dc6ab7168be9b2d0f09ea4a67f258cb81107220262b8e2f4d225e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 KB (241654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47c9a3401c05d7824f54772e0d02570d02c3f55e1fddf78cd21067e60efc5c2`

```dockerfile
```

-	Layers:
	-	`sha256:e5f6a38abac1a17ed1970a8602641e4c4bde399c4196605898a1a657c7e63681`  
		Last Modified: Wed, 10 Jul 2024 16:57:53 GMT  
		Size: 228.7 KB (228702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e031f62d46a6ca4e6de59c0cc988ffbc0bb930393e9118e1d97f0b83cdb5cb7f`  
		Last Modified: Wed, 10 Jul 2024 16:57:53 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:a16a5b57d3e4457d2140d91d028cac459fdcd0ba2ba91d26e5f00b1b9f4bfd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13993934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a390d6f3ea80c42e3e2ed3ebec8f8f36bbbfed5fad150adc99614bdfcb6a7fc5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015d1f69378162b5fa5424cb0003b8cde93cb2285cf91c2306f0563062b3e90b`  
		Last Modified: Wed, 10 Jul 2024 16:57:17 GMT  
		Size: 291.8 KB (291815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9098276cbba568fa3cb9f66584ae02cda51f881e766af1670cbb52940a8dfff3`  
		Last Modified: Wed, 10 Jul 2024 16:57:18 GMT  
		Size: 10.3 MB (10334354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b549ce7cdca2d4dc3e425d5bcd2b51d2de771fdf0fddadfabf516afbd8fad6`  
		Last Modified: Wed, 10 Jul 2024 16:57:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207f6e04bf3789f4bc3715dc9bb1eeeb406bc79862b92a53de5ba32e4959c242`  
		Last Modified: Wed, 10 Jul 2024 16:57:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:df208e8ff557dd386a36669442732b3f0d5ea28aac5069843be99b200a9d94e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824e5eeabe6d00ddeb36713b0d2ce929ad0dbef979419c1e0c87222d1cbf284e`

```dockerfile
```

-	Layers:
	-	`sha256:81305ab993a70212d40a652d83e40a23b8e55c73f157cdb2fd1dca954fc584bc`  
		Last Modified: Wed, 10 Jul 2024 16:57:17 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; ppc64le

```console
$ docker pull registry@sha256:f684b059e1bead536b10df00dfe7844f41913f7b270a4ce69d833b0b427a526f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13787210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c97c682f579291a27bd1a86d107c053f6fd39e50cbf9578da3eb09befdfe77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9f5c2d70d1b2f0680099e2f2c23c65c26d42c697204adc40f230e96745643`  
		Last Modified: Wed, 10 Jul 2024 16:57:35 GMT  
		Size: 294.1 KB (294072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9262d0cfcb4ba2645a1e45185a32b3b150e5a2a2cf28a28a41d7a3a5d3bb0cd4`  
		Last Modified: Wed, 10 Jul 2024 16:57:36 GMT  
		Size: 9.9 MB (9920830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30baab779ca63098d3d098db5842361df51cbdee653735882c020479fe12d78`  
		Last Modified: Wed, 10 Jul 2024 16:57:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81042a1cc53e023a7477b063f5c455a4e4b73211d69c7438e56b89adfc84d6b8`  
		Last Modified: Wed, 10 Jul 2024 16:57:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:a8c46de488e08d8074582c1417d364dd937d1530e21a58e2dbccd75a90cd6586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 KB (239737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eea31203f4ee03a1b30cef0ec986f446983fbd8b7b8beba1417b0cba3dc2dad`

```dockerfile
```

-	Layers:
	-	`sha256:84c3803f90fd67c6d37a74a70e65ff37a6477072ad7c3f6f1be6eddc4aa04315`  
		Last Modified: Wed, 10 Jul 2024 16:57:35 GMT  
		Size: 226.8 KB (226764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8238ff952897a4d600f05363e6fa8e72152862794524ba5e34234bfc140fafa`  
		Last Modified: Wed, 10 Jul 2024 16:57:35 GMT  
		Size: 13.0 KB (12973 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; s390x

```console
$ docker pull registry@sha256:9d21cb7d4f3b0745bc9d429efc108f95511c18b35ba3d9281dc4e6728e9a378f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14299817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e363f04a71f4dc7628ee7424a6ba50baf0d958a7ebc1cb2c6acb4bcc99c00c21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac331ec2d999ec11912d90cc951becc57cc0a546f147316d36d21a37047aa9a`  
		Last Modified: Wed, 10 Jul 2024 16:57:37 GMT  
		Size: 291.9 KB (291940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee89d2d3636d09ffd8efdc1a3eba91901e776f7b5fd56e6f6f80970d6e6bc6e0`  
		Last Modified: Wed, 10 Jul 2024 16:57:37 GMT  
		Size: 10.5 MB (10545411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6a23ff695d37fe311fe1d9640920b718788c7cade798f349cf7a586380f51`  
		Last Modified: Wed, 10 Jul 2024 16:57:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6499f296338e5dc9fd8d55a18a661465dfaf41d6f6dd3a1ed8cbf32fe59f92eb`  
		Last Modified: Wed, 10 Jul 2024 16:57:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:ec6c560950aae44f3cb6db5dcec3fb46f1858648b6b4f62b455b128f54087d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 KB (239688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d978dc9bd1abe043c0789c478f4e343795810fcca13ecec8191bf3db5933a`

```dockerfile
```

-	Layers:
	-	`sha256:9d6539c8b1c5c9b35d70a6f7896599e357d749037aaff50e044091ac86ed150a`  
		Last Modified: Wed, 10 Jul 2024 16:57:37 GMT  
		Size: 226.7 KB (226734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f34ea5d18632b9019416c703f55d423d198d4f2c9464f1467a4259a844976687`  
		Last Modified: Wed, 10 Jul 2024 16:57:36 GMT  
		Size: 13.0 KB (12954 bytes)  
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
