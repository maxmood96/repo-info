## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e2d6df9666d3bf936ff151acaeb51d0f482286eeb9e79808b0b33c3dee34ea23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f97f3a7320d861f816715e01e0f9ab1e57990f9af05b556ef3df340996878768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235142682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82af38e1f389042f9c48299e5be0a30bb5c291507dde14b85ccf33501ce32e35`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd4aed23fd1b7814575cb5c4ed9f603fa21cdc30396915a7b20403b058a802b`  
		Last Modified: Tue, 02 Jul 2024 07:07:17 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540cc6e10574d04ff9b88bee7a766ed9d5b442e9f5f3c78677e646d1f06d1c11`  
		Last Modified: Tue, 02 Jul 2024 07:07:15 GMT  
		Size: 58.6 MB (58624232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27706f8abfc9d9f67753cea5bc15975f4267f0877a566f008b2650387982e40`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5130eb53ad9ec6610e7491d63b0b86a6767f603b8cb9335df9ffb7b264a35a6d`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f7cfc31c15fa1a689f1f25dda2a1aff70057e6e89a7f85417b06b7f858e5f7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c979e1d913d3de7f93a0ba4f0b818952016f11bf59700540e488c617839ea6`

```dockerfile
```

-	Layers:
	-	`sha256:34e7cefa6a70c74c7c9250e3f511e2c4cb93f3743ee323af007b896f041f7d89`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 4.9 MB (4909272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eaa4f97702e77703834b487120a3d268b86497e7329d9a890963b6dfdf02bed`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 15.5 KB (15511 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ea6b7e7e877e583e42faa4246636e5011fae5b1174701667d5770b852160ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232707502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f50fd2617d09ea714592cf5646e3660fb44fd3d0ec3e9e6be183f5a40d5879`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343d2af50bf52fcbb3bfdbf2cbe68f34c183905bca6495e7adb48e9aadb23f0c`  
		Last Modified: Tue, 02 Jul 2024 09:30:27 GMT  
		Size: 143.9 MB (143892776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bf6f0e889bd789d934d40e1f655c7d7f6fb48974672ce85937bb93155d1868`  
		Last Modified: Tue, 02 Jul 2024 09:34:36 GMT  
		Size: 58.7 MB (58744069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99108935d6073fd1db90935b5726735745bd898b22cfd9f79dc1b1eb07222db9`  
		Last Modified: Tue, 02 Jul 2024 09:34:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436927d4d62cca035cf8ba26dd609ed12ed014da006cf70fd134e0ed994c8883`  
		Last Modified: Tue, 02 Jul 2024 09:34:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d48e87d2375f3a96aba2d51e63cade52d4015b38e87520496b88259ddd9519b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2aaf1fd353e8ad4f12c897a6b16eb21f8eec1548d4b2225ddfcce965c45743`

```dockerfile
```

-	Layers:
	-	`sha256:df0b9b75e71bf8611f4cdb416e86e18c9a43998580fcb88b58c9af346958bc8d`  
		Last Modified: Tue, 02 Jul 2024 09:34:35 GMT  
		Size: 4.9 MB (4915628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fa21c3d08430f222653b4e0be9fca93fef52d627487f6e8a68e25dfc845d9b`  
		Last Modified: Tue, 02 Jul 2024 09:34:34 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
