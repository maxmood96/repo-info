## `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye-slim`

```console
$ docker pull clojure@sha256:dcaa4c2360bff71bb4c15e48b142a7f23f84e8b07184e4e9a72b8a2e637a3686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:92f267eee6e8c02208e0855b8ca1ae26196cda5941ccde3aef26e7ecee5ed04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181678912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3a0b7cf8343841cba4bfdaca34fdb4a10e278236ed6725346ec70e7de3eaa1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:57:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:30 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:30 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed082624cfc6c04416259359927805ea5ea6f513aad4f6aae53522df6dcfabc`  
		Last Modified: Tue, 24 Feb 2026 19:58:05 GMT  
		Size: 92.3 MB (92256282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff7d49932c7fe261db55010dd05a90dec61991d0723eda1d4f9e8fb04205651`  
		Last Modified: Tue, 24 Feb 2026 19:58:04 GMT  
		Size: 59.2 MB (59163213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53a2a01d95913a4bd9742e8795384dae68dd6be2659119ec5f7ba07cd2ddc0a`  
		Last Modified: Tue, 24 Feb 2026 19:58:02 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d12bd291779bc9c0e1db30b720d28943d0350f917cb5fa739f2cfb37a6fec`  
		Last Modified: Tue, 24 Feb 2026 19:58:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4b41f6c4f9d394166aa16ca4206c6d652838cd6e8df8f9832f035f7ef4967e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc03c2010234cc06706af2da247a87fd2ab133f42d007b096186881139e012d`

```dockerfile
```

-	Layers:
	-	`sha256:8706f76b9cbcccd7c8ffb99f6a262a5fac5e85270a25cf1906ce959ace1555db`  
		Last Modified: Tue, 24 Feb 2026 19:58:02 GMT  
		Size: 5.3 MB (5288258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d048bce5534e8072f983f71bfe18e245527e9ed6bdc6638a175854292352e8`  
		Last Modified: Tue, 24 Feb 2026 19:58:01 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f05a838f4f7e4d1f4fd9784f5a192b846ee87bb9fcd7ca820f56d48e8b54ad77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179336965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0ed4676739b50d41f60812813349c4b48133b43b3a3d49067356182d35d19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:08:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:08:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:08:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:08:07 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:08:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:08:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6c0cd577c04b6352cb4612dcd2f637c0fa1a583c4694bf032e1c57c62f10a`  
		Last Modified: Tue, 24 Feb 2026 20:08:42 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87aad06a3e000eaef93963b6cf6e3f9e90426ba69d33f9ce6cb2875e9a678e`  
		Last Modified: Tue, 24 Feb 2026 20:08:42 GMT  
		Size: 59.3 MB (59303180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc15376dc4b597f78bdb394d7b6ef801fb6b28ca2be12faa08d8066ce28e62a7`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f76bff6b788ba69583fc5b0f87b7a55fa0d83d9d3642c22970dbcc09234c6`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05e6fc3d640e64ff46e4e042b4be482572a7450c095e5dcb417d3d69218f240d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5310677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ceee04bd68d07238e10925a13de326ea0304b45685967a504842b6b4d24f3c`

```dockerfile
```

-	Layers:
	-	`sha256:4a8299f84f0d6b20c9788d0a5e232d15a7630c86eedf07c19036b362b1938670`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 5.3 MB (5294011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efcbc1fa885d689b138c374bcbfa033855cd91bde24a446c7350e2db97cf8f1`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json
