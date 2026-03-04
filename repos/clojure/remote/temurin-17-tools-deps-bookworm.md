## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f8b49a1d25a7795c8e712866e494e0e65b21ef57c2ff00aafe24a49f23622aec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a0893f10fa3ebe0fe3a375002bf4e7d2855f7ec6fc11955f0beca21d5837bc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275295997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae241c9c560a7ff0b5ea08b711b02bf9d8b578325a5ebe2a790768b1f6d80ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:49:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:53 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:53 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd2e9a0f055744cb3fa8ed34310bec4aea9e8eac62f2e7f4ca02c5e987bb560`  
		Last Modified: Wed, 04 Mar 2026 17:50:29 GMT  
		Size: 145.6 MB (145628732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f7decbe868bc1fbe0de5bb6f425ed87b94e36d61479af51f8d66e380110a02`  
		Last Modified: Wed, 04 Mar 2026 17:50:28 GMT  
		Size: 81.2 MB (81177444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b98b5e46ae8498e6b2968584bb9b7580092dd76e233f9df387c00478da30926`  
		Last Modified: Wed, 04 Mar 2026 17:50:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249008f24628e9b99a649fe67a36d3d448187304b0b5296515070a8b7aa13c9e`  
		Last Modified: Wed, 04 Mar 2026 17:50:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:23d37b863122bfb307aaa736c86845ae157118abe7a8f86a3b7773f8fef00943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d22908a3eddfe4a2ed8b3f44ff8c699ba6c1fe6021afb0f7ad5b814f2911bb7`

```dockerfile
```

-	Layers:
	-	`sha256:9621625237c92b20884f80964d8346d37505e92affe2d4240e6774f9274a4b1c`  
		Last Modified: Wed, 04 Mar 2026 17:50:25 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9cfbef2034c7377ae7f5a527845a29f4c732943b7cfabf0333564dcd9ad3a0a`  
		Last Modified: Wed, 04 Mar 2026 17:50:24 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:772dbafffa809ae2f532cc29157cd14e5d6452d77145e6091c9120cdd9365c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273968462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c422e3c1358403d823f9eeaf5082eed87239b4d6696e81a832c8dd2ad306e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:49:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:39 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:39 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:49:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:49:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc738132e8b10a1a99e52ec7fc31e82c1d70a503e7d994da0cbf476fe66bc0e`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 144.4 MB (144436183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d4001bfac06611e1b1a755b3a972c06c8ce9bafc19018424071797a9c6642`  
		Last Modified: Wed, 04 Mar 2026 17:50:17 GMT  
		Size: 81.2 MB (81158027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f3dac497071c6caec85fd41ce3abba76c4ffa265e6dd32dcf448f2d7485f73`  
		Last Modified: Wed, 04 Mar 2026 17:50:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd06f2d44329eec64e17fbfc01a2562aba696b6297cb0db68ca30b8468f35703`  
		Last Modified: Wed, 04 Mar 2026 17:50:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9df99862f90c1a9d1422d1217013f36ed1ed6546414c1a0885accfdc4db20df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2996b0d43af8de96f4fa76f50e11e9786fd12d6470856dbbf253b0001ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:e806b5b8d9f64ee157e480c034408d4fd0be5cc416af3a8cb707c8478b80263b`  
		Last Modified: Wed, 04 Mar 2026 17:50:15 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7bb8a925f20b497587dec4f39d3b5e6460c9255832bcb4b06cfa47018f4929`  
		Last Modified: Wed, 04 Mar 2026 17:50:14 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9de9c5b7be9d1a2edb0189f8252fc219c50ff1a2fa25ab0238b4b6b128a50672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284776302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d7f49e68ee65a7ff1d8b981f1640703cd05424bad54a95628a5e85a9cc44ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:57:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:57:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:57:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:57:08 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:57:09 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:58:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:58:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:58:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:58:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:58:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825805ad2dd3d385420e93790c7666bb0fb6dec647f62702d34b61b40720d410`  
		Last Modified: Wed, 04 Mar 2026 17:58:56 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35dd0dc35b34ea4749f8a7444e8212f34a0796d2d638cf79f81bcffc87cf19`  
		Last Modified: Wed, 04 Mar 2026 17:58:55 GMT  
		Size: 87.0 MB (87000210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d92d3e7a690f4382e24b09aaf07cc1e9f11ea9bf86c0aecb1a3658e49871b2`  
		Last Modified: Wed, 04 Mar 2026 17:58:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee84f6de25eebb0f202d31860f8ad1a15f766cc477ccb238f6f56c0f51a55c88`  
		Last Modified: Wed, 04 Mar 2026 17:58:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0ffd3b8a73e068ed8a3904be580965b87375f446ab463e5dfcaaf6e2c5ad2daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110446dd2071105678bbcd0f273db576d94320b19f040089032076511a3a3d75`

```dockerfile
```

-	Layers:
	-	`sha256:e9f881596dff1ac7eba864d90f747e44d6555a53fd9392f5cf9fe00e4262eada`  
		Last Modified: Wed, 04 Mar 2026 17:58:51 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a3c695040da37e7510505ec7b63b6e85564c8e924c7e076af905e71f960f0d`  
		Last Modified: Wed, 04 Mar 2026 17:58:51 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:184967e317eba2014e54789f68d27beb98cd208e2adeaef35f164226fea900c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262764363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94aaf9a9b342f9d203e7fbb76b6e5b368dc7a3e49b4dd2cf1ba09c4211ce3949`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:14 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:14 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:48:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:48:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d912969471f33c049367ed8b14cb8e8c4f21167637003f373328d4541a69fa38`  
		Last Modified: Wed, 04 Mar 2026 17:48:58 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ed9d32a160bef25378c9eecfc82f167ab40bfa7e242df53128fbd418748ccc`  
		Last Modified: Wed, 04 Mar 2026 17:48:57 GMT  
		Size: 80.0 MB (79988120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f56547c30b31cd7460618a8adecbcfabb6121c0c185a163c3bed1011091d98`  
		Last Modified: Wed, 04 Mar 2026 17:48:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0545317950ad5d5d265574135ffb5605b9a17ac6eacc0f4e8d6296b7b79c6`  
		Last Modified: Wed, 04 Mar 2026 17:48:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:83431e7ce4c93642725cbd4595794bf7f4fbdaf08d8b2b0e7a68cc2c4c862fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875e09a3630df72e79a4ca24a951f2cb0b07ee222f93165be794420a1794f11b`

```dockerfile
```

-	Layers:
	-	`sha256:679d57af2d42c03caf202d7777136b087a3e1a1102c76a66811560b7dd1f5d12`  
		Last Modified: Wed, 04 Mar 2026 17:48:55 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c345d53466bacf2fb2a8105ff01528a86807d1309db66f11a0579071c71eaedf`  
		Last Modified: Wed, 04 Mar 2026 17:48:55 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
