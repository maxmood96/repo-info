## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:c6a1aa52ad345605a6a48a2f1edb1fb16829f5778af3f55494ea226188e13996
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:26e8f1958a5d04abca4aea60dc80cee1a083a41099eb11d7d1f2f2a67a99bfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178050895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8580b13def2cec3f9a284541f26a0a2410193a37f9877dca9a93ab4a1118fc8d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:50:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:50:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:50:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:50:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:50:00 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:50:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:50:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:50:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbe9b6b752292936de54d7ee17e2b8a15e35108a88db7071c8bc7b2c606eed9`  
		Last Modified: Mon, 08 Dec 2025 23:50:43 GMT  
		Size: 54.7 MB (54733370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0243c9a82f3f230e939a58ebca8af8ca085fe2f69c56def9d0a245a70f195a2a`  
		Last Modified: Mon, 08 Dec 2025 23:50:47 GMT  
		Size: 69.6 MB (69560469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98673c5849621fd423d29b9cc5577d658a7b0a8e5bc9d9e2daec78a83055ea9b`  
		Last Modified: Mon, 08 Dec 2025 23:50:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0fc98c7bb6049cf56b3a3a1edf0f348bd6ff35bfe8fe9eef4a1bf51288a51def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974f50fe7bc083aa13a7fb6468f58ca92e2fe04e3f553e1f50dab9dbf078a85c`

```dockerfile
```

-	Layers:
	-	`sha256:7980b8c84a28cd0e82f3e4a900c9133a51b54016addc951cb63e56bc50a07985`  
		Last Modified: Tue, 09 Dec 2025 04:48:07 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53afdb2a6fb169cf90d39058fe6e1f911415cf7e59b5223a36a580df6bd81998`  
		Last Modified: Tue, 09 Dec 2025 04:48:08 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:14dac349699c75b1a8e0a720b18a1b93e61df7d8b1570dc8f7c4269b85e34b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175761586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4480c1f5f1041e07124d89527ee5b8698bc98aa0544adbea55a42f97c29057c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:57:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:57:43 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:57:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:57:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3a774c2ece2558446e3305d05673173f46a6d6f1d6967ead555e3ff19deb46`  
		Last Modified: Mon, 08 Dec 2025 23:58:28 GMT  
		Size: 53.8 MB (53814983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e65e3990c5c191f7dce00827366515f8de5cf9641962c016e572c61db537e7`  
		Last Modified: Mon, 08 Dec 2025 23:58:26 GMT  
		Size: 69.7 MB (69688243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3ce06148292ebbebd94329d23e3e2e4ceb4c0036129568155f4317464a841f`  
		Last Modified: Mon, 08 Dec 2025 23:58:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7a02f9ef683b6ac0eeba7d949a0b3df4b479de229db92e959e961e1f2d8713ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152e42ed42b657838d5bfe4fabfa2b65119778194e1b300deb1829c5b9cb04f9`

```dockerfile
```

-	Layers:
	-	`sha256:3fdd056533c762c7873a9f6e677e8dfec4c6750c3cb33bdaeb8545d6e9b5bc5c`  
		Last Modified: Tue, 09 Dec 2025 04:48:15 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25b3d16dc48b81e6f1e38bde342544dd4ba87ee002c85aae9c4268e6afed893`  
		Last Modified: Tue, 09 Dec 2025 04:48:16 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
