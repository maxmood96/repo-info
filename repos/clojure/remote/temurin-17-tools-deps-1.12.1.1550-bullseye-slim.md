## `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:9be5eb8d7853a30f2d65b13fdea347d8d266dd8bc315eea5be3615007b89f629
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fe8a0e0d424d80bebbe7889ebab79d88bcde27fb2f2095ffe2cfe72cf02e47c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233897672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0273bf3fbe8040df67b01727a6d05f148e6ba8c196258ead7b5cd50d1be8be4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89892b989d441d98f7a564857ffafd5632c0d6fa2aa22fd18ccff44a9caa593`  
		Last Modified: Tue, 01 Jul 2025 02:39:33 GMT  
		Size: 144.6 MB (144634948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ec713b7515cbcf2d67fd13d11ec9d853ca00833b39f83c1c58b91c9dbdb2b`  
		Last Modified: Tue, 01 Jul 2025 02:39:45 GMT  
		Size: 59.0 MB (59005637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e71b9e6890c90e200082771d73ddea2c24be91d3d554427ddab9004e9cd450e`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2ad657f21446a9b69a2d2e1612c055f593412f3c4ccf532eb491fad6861af`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2f6892026c3bbe3979190af97d327d3f25d6ebf3e5a95b271f6b58a25db51af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ea4828a4a87b8fad3f147e0b0cec02f5d5b81dc36cd0b3277323ebd8d57a1c`

```dockerfile
```

-	Layers:
	-	`sha256:4cd2a4ebcd1d219d0ae06e64b866ed5c4ba76feec31765923691dbd6cca6b8c3`  
		Last Modified: Tue, 01 Jul 2025 06:37:07 GMT  
		Size: 5.3 MB (5308038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5685c82944b6ff835d8cdd0c18762912160c3124ca988b76a52e27bb00100cf9`  
		Last Modified: Tue, 01 Jul 2025 06:37:08 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:023565d861336b63316d1103c42210e3a389aea07b49e7e1598614c0e7c6059c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231395498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e9b6742f0cbeca843626d1567e817f95168c88800910728c2c00ff626f8de9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4597b8d774c37ff2a36ab9fe4dba1a924caaed8279e24328a0e943dd6d2da`  
		Last Modified: Wed, 11 Jun 2025 05:54:40 GMT  
		Size: 143.5 MB (143512642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15adf44f9028c1ffdbfcffb6fa411a17c7cee7bacb163df4af9a8e3a948242`  
		Last Modified: Sat, 14 Jun 2025 08:41:22 GMT  
		Size: 59.1 MB (59137631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4100f0b2e837ff0bc1d8d5274fa7c52e484f9a0d23d3090606929556f9abdd3f`  
		Last Modified: Fri, 13 Jun 2025 00:39:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d6c7daf97f0513f18348fd31df9e83af4109fd5773d57ba0ecbc7e5948549a`  
		Last Modified: Fri, 13 Jun 2025 00:47:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:258dc1d668b9bc10f76a8b43b615158c48cac90b8e30d82ba6f1e61af709fbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f30ba4bc942cb91a11ee899d15d9c3517b5593490bd5602e55fcb43d3cbf62f`

```dockerfile
```

-	Layers:
	-	`sha256:9a81722afae427e75bc28eea405fa32c694702d62d3ef435367681500ce26bc6`  
		Last Modified: Wed, 11 Jun 2025 09:37:31 GMT  
		Size: 5.3 MB (5313770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e111ed09e6d73fe5564218bfdb29b278fdbe2595bc8f26e6119769e006cc9a56`  
		Last Modified: Wed, 11 Jun 2025 09:37:32 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json
