## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:1effb9465b796fa970710ceae94b4dcffd9ac3868984eb95796806e3809a6a79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ff8556e20dba651ffd6215bac745e74c1b746ee0629debeae1c783545be60f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268007116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c490a5a4cfa223fd8d91a3b3f1555c46b246439cf5d45cefec529a6a8cdebc6a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360982738cf3dce18d3465505964b901dbafed3f7e43827cb99aa58addc437a`  
		Last Modified: Tue, 02 Sep 2025 00:17:51 GMT  
		Size: 144.7 MB (144693323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b408713752cb0f920f26d67d2fff977f0d8e4828eb1f8e18ab63a2a3f9bb5945`  
		Last Modified: Tue, 02 Sep 2025 01:32:06 GMT  
		Size: 69.6 MB (69557403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1b813252a6407b21f0dd0e0d8617bacdd0cb7f0fc1018f0bf399b562c01e1`  
		Last Modified: Tue, 02 Sep 2025 01:31:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c2147d7d96d380bb6c8d54a2fc3f674adaddb362a5fe6425e5f38ee5d2b076`  
		Last Modified: Tue, 02 Sep 2025 01:31:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:158fc0b2044027e8f1a07115d7d4c3924c3d06cc7cfaafac972351da77c5c66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df75bb109aae72eddb0d41419082a308b90794bf563a46e6f730946739bd8354`

```dockerfile
```

-	Layers:
	-	`sha256:19b1208ebb1ca7232b4689bd77c3a919c41c2add3127d239134c7d5c5af22406`  
		Last Modified: Tue, 02 Sep 2025 03:38:10 GMT  
		Size: 7.4 MB (7395667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d05d5fb501892cab21288a8e6a806773014b7213a8f48a1098dfa68aca07af0`  
		Last Modified: Tue, 02 Sep 2025 03:38:11 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:229a2c9aaf8ada3dadf904c87b310a25aeae97f92e9351b3fa8a53be251cf231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265475527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad657a9876473ab8ab4f4b9c429d973a73d72b5450043229dfc75638338ff752`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df15f2eff937c38546ced8d4865e045d0e5e6d5f3bc0f26200a5c72c013ca2e4`  
		Last Modified: Tue, 19 Aug 2025 03:49:08 GMT  
		Size: 143.5 MB (143542129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437c08ba1934df8c25531da7acb51a2353584a260cdb7f5774ac8d84ee60a28e`  
		Last Modified: Tue, 26 Aug 2025 23:12:40 GMT  
		Size: 69.7 MB (69683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1045d13bcd4c230753fc6fe1a9c042baa3515f15d866fc67c4d30ffa0f20febb`  
		Last Modified: Tue, 26 Aug 2025 18:34:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d498d6a4523fbff269cfa4ef81d974d0c862e2a745a19c52356797a4d01fe7`  
		Last Modified: Tue, 26 Aug 2025 17:42:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6eba673385d9f5f5a2c8a67cb9b6a6051734aa693451d7ef30fe4ef5aba98922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ef311aaa1256fd0c68c13cf7028e127e5c31aa5181b472397321dc8d3251d1`

```dockerfile
```

-	Layers:
	-	`sha256:966103546bdb6c4cf082735f2c70d5bd5c919cdd883cc256b6beb8de63d15dd6`  
		Last Modified: Tue, 26 Aug 2025 18:37:44 GMT  
		Size: 7.4 MB (7400766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a9e6442e4f803fec7c504138b5bb68b4f55d903c64a2c8fdfd69f624ea3e1c`  
		Last Modified: Tue, 26 Aug 2025 18:37:45 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
