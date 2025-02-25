## `clojure:temurin-21-tools-deps-1.12.0.1517-bookworm-slim`

```console
$ docker pull clojure@sha256:52ffbd8f81276cd91ac67190af8a42d5845f2d3f0d957dec7c91d670db50a0eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1517-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7033036953431abdc2286a2b208accc24805ae3e8daf7044409ad0e8130bc42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255336022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a17e3239b64a7ca336e886653184180378beca55475dcd128c06053d83e6ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1b893aeae12e7e0e13e0dce43f3f67c97cfbff10ffe22132678a5362df36c0`  
		Last Modified: Tue, 25 Feb 2025 02:34:13 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf57137c306279d421f5d134c05f6ae0054125eb87774443f40ffb35271fe3`  
		Last Modified: Tue, 25 Feb 2025 02:34:10 GMT  
		Size: 69.5 MB (69529792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7fcb26c0d5a74c652c691a0cebf4fc0fdab4e29417e8b8978e10b224fa380`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05117f64d837d11aed1434bb403be814d730a4618dddc63661e2b8e02297ff2`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64d61b86ad39a42420b88a797c3448e19186e52c08ef5ce2a12d8772e519a1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094171322685736558b7faa57611a653c22e35af246aa8d7f246537dd536d2e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a1ce544136d1c71702dac2233a17ba83860eeb526c9c6f1700bae22b1bf9261`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 4.9 MB (4916383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214a14ea97c3c0342bbd703c43a553896db481c9eed3d1bce9432fcc09b4efc0`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1517-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:482e7608138b47bcac17def93abb61f2fe777a1ac4e7fd4099635364fef0c11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253280682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6be5ed6258388a6bcd4f38a87c08e0d3ab9d03b353243fd70d9bf9fbf44128`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7350927a264592e316264c7cd122bd538e575003045857f9e107bee0b62198`  
		Last Modified: Tue, 04 Feb 2025 23:52:12 GMT  
		Size: 155.9 MB (155859249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25cc32a61aa0b19eaa2f6844d5490711e58df067cd6fab69181bf7c9d021ac0`  
		Last Modified: Thu, 20 Feb 2025 03:56:56 GMT  
		Size: 69.4 MB (69379513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78abc7e31c39213f4bce4a0662f978f5e7eff10c177e49f9c7c4a81e23787705`  
		Last Modified: Thu, 20 Feb 2025 03:56:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b7ffa729aa153006dd15e20ba924607fa63d8ceebadc47c07c1a77a3433548`  
		Last Modified: Thu, 20 Feb 2025 03:56:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c236b82f00e24575b1776705d73c1a04ce9a501fd1f733b26d6fc3203529eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20de77749010a406cd37395c246422526e7536cf53ca2fdab78d0e1bfaabceb`

```dockerfile
```

-	Layers:
	-	`sha256:7ea2dc609f6dec463849d86e2792ba9f563c9eacf54ba63efc4b58c7b770bbfc`  
		Last Modified: Thu, 20 Feb 2025 03:56:54 GMT  
		Size: 4.9 MB (4922150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309cf9462f17e8063afb9f6c5f26becf657008ef895e505186bf2ecf538b39ac`  
		Last Modified: Thu, 20 Feb 2025 03:56:54 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
