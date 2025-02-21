## `clojure:tools-deps-1.12.0.1517-bookworm-slim`

```console
$ docker pull clojure@sha256:42686a34213018c4de0ddc4363dc9dce0d44fdd23b8737626371c619b9c9ab35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1517-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7457e3d0ad571c554069c12672d69317b9b7d613649bc4931be58565ec0eea1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255329598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae09f6f25c77a8ed936cb6173d953bb46656150f01e0d41956f3a2366aa508c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a119698ab625dfc669766243d1b5c44d0a8f3b908d0a8fb16e1d0348fccfc3`  
		Last Modified: Thu, 20 Feb 2025 02:31:03 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9ab4870fe631b8977aca43cb1c8f5607d17aa67466148dc4c65677dac36636`  
		Last Modified: Thu, 20 Feb 2025 02:31:02 GMT  
		Size: 69.5 MB (69530370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee83124977023eadefcc49a33b44cf02a0a9029c65f4766bf6487ba3ef5fb0`  
		Last Modified: Thu, 20 Feb 2025 02:30:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f0ebed4f5083fa47c94ff09e916a9b0af9ae41cec79c23b278182a141c2d8`  
		Last Modified: Thu, 20 Feb 2025 02:30:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04f25cedceb1665e54445f4c2eaf37b4bfebc410e998909450c814799dadb139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab416851111d23c94cdb61e8836beec8d1ea75ef30a4fb96d06ee1a243523eb1`

```dockerfile
```

-	Layers:
	-	`sha256:a20fb0118725279a0bbafe3f20847dc8f34329c0d8be2955c70df6d50c5fcf69`  
		Last Modified: Thu, 20 Feb 2025 02:30:59 GMT  
		Size: 4.9 MB (4916365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f49c0a23470184fc4bbafdfb02397a26884566b3062cc8ebe9d6360a21639d`  
		Last Modified: Thu, 20 Feb 2025 02:30:59 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1517-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

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
