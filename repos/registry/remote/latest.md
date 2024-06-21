## `registry:latest`

```console
$ docker pull registry@sha256:18c40c73e49a5f9febf2e4cafa57e4bbf14f343745c70317c2332bec473c5f7d
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
$ docker pull registry@sha256:53ee3286cf0400c2ec957e31594c77439ec959e26ca00c8264c5ce521f7859ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9454531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27031dfcd859912546a3d00ad8ec0579adaa81f85dc9ff6099698a994b688203`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e2c05bc16cc193218be487e39ac3caae6592d57307aaeb0410a43abfcf4858`  
		Last Modified: Tue, 30 Apr 2024 18:11:39 GMT  
		Size: 295.9 KB (295853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6122473202ea088b18b50b2a1156df1b918803043db153f5cb6add1c30539d`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b06a7c7f2a2124ea42b973fed091d2da803e4c844f520befb1ca70df254c3f1`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2824145f0244c1b3a324cb349f251167c79f18c90d0deee54b55a1e7a4604dad`  
		Last Modified: Tue, 30 Apr 2024 18:11:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:ddf16b02d59316a6cd9e7e1467f7e3117fbd6424f51262ea824c422551099014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 KB (189989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7f9db154703cba3c714a2d5116640d2017e5be807331430c60daf1eff8441f`

```dockerfile
```

-	Layers:
	-	`sha256:7a8be2171155d1d5edefa6e9af949ee399b8830b51ac0848ec45173f73f41c5a`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 176.2 KB (176226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16163694eff969f7c48d7d2a057ec6c54159f1217b6c13d2ede970a49c386e3`  
		Last Modified: Tue, 30 Apr 2024 18:11:57 GMT  
		Size: 13.8 KB (13763 bytes)  
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
$ docker pull registry@sha256:a84825b3ee8d4bfeab7ab0fb9a4893ae9e9bd19590f09edde4b835f3b2a6bb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9672089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610cc9b5134032c3006fe91c0111bae98daa6e3755a35dc563e94a5be2a3342`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
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
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee22372c95aa515952d82e996ea552219f8b8387e28a7784302551be5e80c1e`  
		Last Modified: Tue, 30 Apr 2024 18:03:10 GMT  
		Size: 293.9 KB (293926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b9bb64acbc685cba56c4e9edcda4189534db0a66b2b54f27da1440bfbe3c8`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a6fa86f86567634ad8fd16d47351ad962259a48cdf8689a168cfa85687d52`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce941b533ba0fb8619f71bff1d9098248ca5b054e5787eb4c079aa1fc89fbfc`  
		Last Modified: Tue, 30 Apr 2024 18:03:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:a46e453e7925f04a3487825874995f0556221da3b526d5f7c654fc695bd5cd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 KB (188014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626b1303784713792d93804a728bfc099e72ca8498612473f26f13e6dbfa6681`

```dockerfile
```

-	Layers:
	-	`sha256:427ef25a040582ac19cb182432b0a7147cd5f54ba10b291bced28fd287fd9f6e`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 174.3 KB (174261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ceb9142e1385ee46cbaca350dc69d6dd0d5d1fe588b6b7714b8164878d20c91`  
		Last Modified: Tue, 30 Apr 2024 18:03:44 GMT  
		Size: 13.8 KB (13753 bytes)  
		MIME: application/vnd.in-toto+json
