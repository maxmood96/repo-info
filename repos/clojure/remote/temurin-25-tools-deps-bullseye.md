## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:2d116f2fd48bb91b3745420b857670556a75a5bf82f60d8bf49f8308fb40e94c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2c467586a1a6dc6c46c51056f344db6a8e9cc97a72360df022084bbfe6fd6122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215353684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94f5a39f69110fc838ac57749c952c3436a69b400dd0d302f324b8305f4ff85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a6377f48054870d07fe159965a56d2ef01bf1e988e495b154857e401123c7`  
		Last Modified: Fri, 26 Sep 2025 17:58:29 GMT  
		Size: 92.0 MB (92036048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c6d322f29b79e36df1cd465824fcc01e4bc6bcec7f9a5c620dde2d21eeee5`  
		Last Modified: Fri, 26 Sep 2025 17:59:23 GMT  
		Size: 69.6 MB (69561195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68772465603dfa2e7379d76941b4b5577f5d505ccb50cd55c77154e288bd40e`  
		Last Modified: Fri, 26 Sep 2025 17:59:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38743d7d0f20206bfa319c8bb1ce95be39666f8c56baa029ed3aa3adcdd89716`  
		Last Modified: Fri, 26 Sep 2025 17:59:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fc2b2f77fa20e5036e027139aa48282f21c7bd2781c9d66bb47f865e5420dea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd27503e44fcab58a3771d479d51a587d76332df01a4928484d244a424c91e7`

```dockerfile
```

-	Layers:
	-	`sha256:2a7c3211750f2cf308a6740b015fdd8d38b455682f93eeee23fc05547eda22bd`  
		Last Modified: Fri, 26 Sep 2025 18:43:59 GMT  
		Size: 7.3 MB (7346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c7a6f1f97ce2dfcc3cc7d18b5b033873560a80365ca9088169754c014cb754`  
		Last Modified: Fri, 26 Sep 2025 18:43:59 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21a3512799a1748d05b326424bf24720a492983c600d6f517ae3e675b36be862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212983149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f559a857a2c5bd7163ce5c1af8c9c08f494c7978433808d6b5be9e3140b808b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c79da623ebb8ed23fa67b62312631ae068565467408340d717026bc7b6009cd`  
		Last Modified: Fri, 26 Sep 2025 17:57:12 GMT  
		Size: 91.0 MB (91045230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbe0f9449b2734fe2bc4fff6a2a5c3c9aba82aca458b3d1fdac95de7a64f785`  
		Last Modified: Fri, 26 Sep 2025 17:57:08 GMT  
		Size: 69.7 MB (69688504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6eddad311182cf3d755d42a479575f6381c47aeda4b50db4d2888fb53d4842a`  
		Last Modified: Fri, 26 Sep 2025 17:56:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8821f2b090b68e3fd809cd98d2b18951f89e6a83259b7091753a6876741fa891`  
		Last Modified: Fri, 26 Sep 2025 17:56:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f0a7f19889e9f6370e412e54b4da72b22211092e7b9fb769124cc53876fa97d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cbf86905c58993fd8431807d32113d0900bccf1a8e681e65a4cf1d3b28e74e`

```dockerfile
```

-	Layers:
	-	`sha256:ec353e2f437674373ffd4432ab3dbc46ab4a965174cf4e3900c12d65170017d9`  
		Last Modified: Fri, 26 Sep 2025 18:44:06 GMT  
		Size: 7.4 MB (7352113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1def3cbf7d062037d33d5dceccfc34a946f464d7bdaf6d64d688b33ad2f6cc58`  
		Last Modified: Fri, 26 Sep 2025 18:44:07 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json
