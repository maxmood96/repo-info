## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:1181ec4d5b4b7311b4c597d9c177958cce40a5050ec47fc32c622119f5b2d91e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3cc1b8afb3dc7af30bb3897037d615b6114f0eb95f76f44310b71d60e3384b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259113966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e75ac76cf5c3ff81443153ee52593000b1bb40010a6b57607e63846564e41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
	-	`sha256:6f052c0ff895d860a8f6983dcf5207c5e8ff5949529101bf68c1e92e9c8baf36`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 29.8 MB (29756816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027adf75a7eb9c545bb493793343135aacc2f94e096267d4299a0650262d7402`  
		Last Modified: Wed, 11 Jun 2025 03:43:51 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787040c641380e8751a3817430105ac45636b9fcd804102bbde09d88eb23a72`  
		Last Modified: Tue, 10 Jun 2025 23:53:05 GMT  
		Size: 71.7 MB (71721606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1358338613bd9d2e202ecd4b0c6986cbb168ac89e05455b2ca14155755d7f55`  
		Last Modified: Tue, 10 Jun 2025 23:53:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883f07dff9e947dbc706936243ce378948becc1c98247cbbf34de67a360e4ed2`  
		Last Modified: Tue, 10 Jun 2025 23:53:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5824ef76e18c6e41fb84c052b6e62148cedd37c17e0436d81bed4d2b916e9ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b163012400875c99973b1c583d32e9421f3233169e0990489bdfb4b851369d6`

```dockerfile
```

-	Layers:
	-	`sha256:01e10e9472ea9e201858cc84965deddaff37027be9de965a696395aeab318b56`  
		Last Modified: Wed, 11 Jun 2025 03:39:15 GMT  
		Size: 5.3 MB (5256588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eef8c6d00fc3eaa434a6249450f63e3598ef007cbf4df5a3da7ad86450ce61e`  
		Last Modified: Wed, 11 Jun 2025 03:39:16 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03cee0b39a0b45595a0a23cfba88b224ba8b382979fe73ec08562c74bbc2c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257718113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaaba905070236eaf732a54acb90f1e216dea0b5bb6f083cf38c655a78611c16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
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
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a51a9ac36170cd87449a7b39037693e8c1ce7a4b5625c340c05af470954b06e`  
		Last Modified: Wed, 11 Jun 2025 08:36:37 GMT  
		Size: 155.9 MB (155928799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134f08795483c836143dee8cedafc23f7029970a0f92e73bbc8d0ad8aef6b291`  
		Last Modified: Wed, 11 Jun 2025 08:41:07 GMT  
		Size: 71.7 MB (71667229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160482f413af9643c3ad321fcfe565b0fa2f2c79dff289efe42289696a5ec9f0`  
		Last Modified: Wed, 11 Jun 2025 08:43:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231405e4c9d60ddc8a5a5e5873e2f5dbd7d761eb48df7b3db21582fd28f9f0da`  
		Last Modified: Wed, 11 Jun 2025 08:43:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:698c49d54f19a258dc22d8511ab4dc6716f9bdc74a59119e00c0e0d4b7336f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d57b253333f87c9f9d569084ec97d21be6d05f19b56b0a9a5d337501675c88`

```dockerfile
```

-	Layers:
	-	`sha256:9a96f9be67606a9aa58b880f8f784afaf1bcb782939744ac5d6dc777da81310b`  
		Last Modified: Wed, 11 Jun 2025 09:40:22 GMT  
		Size: 5.3 MB (5262381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9acc892ccb8611d4586f83dd391da074bcbe6e4e9ca163881ab5c94fb521006`  
		Last Modified: Wed, 11 Jun 2025 09:40:23 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d9e85c320ea6700e6c75f34899ce44664ce6c30ee9f493e9e3c27f583abe6902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268622607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df26e4933bfb80ad2dbfa506cb60d7a9c6b2b27d3fe5a531d00bc016c7a7273e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
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
	-	`sha256:9851a8240d92395a99e35175026ad70b4eb50fb4e03132b209af1bf02a1fa307`  
		Last Modified: Wed, 11 Jun 2025 00:37:24 GMT  
		Size: 33.6 MB (33580925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fb82e2d496ce339227e53dee24cbcb722fc46228bd3f383d4c1ebb2add348a`  
		Last Modified: Wed, 11 Jun 2025 08:43:49 GMT  
		Size: 157.8 MB (157804906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1832594b52d02bd275a6de2a2818c907104b1d67865b40b3210abaa0e64acf11`  
		Last Modified: Wed, 11 Jun 2025 08:50:15 GMT  
		Size: 77.2 MB (77235735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f6c88b79713b137d6760339d82d6dbc50cb7d5525b53fe6eeae65a1a218c07`  
		Last Modified: Wed, 11 Jun 2025 08:50:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a3cfbd098242d502b7c26f4efb653e7e65bb4c4cd5e5556f6c58071221810`  
		Last Modified: Wed, 11 Jun 2025 08:50:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7979bf33fbfa14055c8c55596fc5cb46ccb0d503c5444794d4fde58c0c272363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb63e67da6e768242fe821eb64e3c942fc0f5b557a2e9d6e8a2b2d449ff71b5a`

```dockerfile
```

-	Layers:
	-	`sha256:578863fa939e53872c3bf0a31c0510fc40b999b9b757845a9775cdcf7a6f55ff`  
		Last Modified: Wed, 11 Jun 2025 09:40:28 GMT  
		Size: 5.3 MB (5260971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e453487f4c91309f19d097cc4f49a3d1ac60eed1625115c92677150292506b14`  
		Last Modified: Wed, 11 Jun 2025 09:40:29 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5018be5a6d5622e0ba999fa2b6f462f6e438d0fb55ae4983734d8b8e622dcb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252411866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cbbcd83efc35518315457fc96954fc07829fc893aa71b4696f2b4803c3b286`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
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
	-	`sha256:3a4ce3b49438d6e971d6a25501e5ee98899a309dea36cc03fae31602fe4551a7`  
		Last Modified: Tue, 10 Jun 2025 22:57:56 GMT  
		Size: 28.2 MB (28247070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39fca1c5edc9e41789080ae4d2069c8256f0ff5e3b91de1cf94cee501e22b5`  
		Last Modified: Wed, 11 Jun 2025 08:34:05 GMT  
		Size: 153.4 MB (153449632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5603ca9ceed3abb1642c646698ba8a463f322eb509e5a8c30955449c8d2a6a2`  
		Last Modified: Wed, 11 Jun 2025 00:35:56 GMT  
		Size: 70.7 MB (70714121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d18453928e09db4c0b7d6e6a47c07bb8140d4864b29fb85f352c713b16f90`  
		Last Modified: Wed, 11 Jun 2025 06:39:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687e012e7d7c40b687deead535fa288ca624bfbe984875f74b92af6835987018`  
		Last Modified: Wed, 11 Jun 2025 06:39:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f26b1395fd6ff96c1b9f26496ae7e612a9dbac746903bf9bbb6f144e671f824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b809f821ea66387d7bca587637d92e201841d8ed3192b7ebeb1b2bd331626b`

```dockerfile
```

-	Layers:
	-	`sha256:305533aee62a634ea7532d122ed06e3381a1bb90dee1f793bdd28da9fafe45ab`  
		Last Modified: Wed, 11 Jun 2025 03:39:28 GMT  
		Size: 5.2 MB (5246064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9d3d764700b6f096ec3ceb6cc3da6c5e69bcbfa9f02be970e7162e1daafc55`  
		Last Modified: Wed, 11 Jun 2025 03:39:29 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:062d3e24fa161afdce9a69e225dab1dcf36dccc3e8599cccd3ba8e3777f9ac00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249564163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099530955bcbd9c8c2d2f6da95cb6a2e9ff925672980e478d25605d642de954f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
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
	-	`sha256:c274825e96bcfbbdcdc116bb72e2d5d06d51048380b2fb22f400e6f9627616b6`  
		Last Modified: Wed, 11 Jun 2025 00:37:39 GMT  
		Size: 29.8 MB (29831871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45021c7f7281fd7e0bd66ca1c56da1f0f7b0faeea6a81d9a5b224fc27237b729`  
		Last Modified: Wed, 11 Jun 2025 08:29:02 GMT  
		Size: 146.9 MB (146911003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587826f4117b00ec24bb4eaf1e753fb7507b72f05f60f74a1aef73867399a95`  
		Last Modified: Wed, 11 Jun 2025 05:56:07 GMT  
		Size: 72.8 MB (72820253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30121fd0fe25fc369042764631849ef8f8a8ab9e3d008a79f2a41a2733eb400b`  
		Last Modified: Wed, 11 Jun 2025 05:56:52 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ad9be81ec992f210bf8f27483d1a6e8dd105a39f8b324baf945fc3885fef10`  
		Last Modified: Wed, 11 Jun 2025 05:56:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bbbd883f1a6688c92bad751458ffe0bf602f6d2212ebeb51efa8f1b474bd29d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b4f82c094f5d2adf1aee9efd73aa66bf347d71c7ee27bed14017a223ec0957`

```dockerfile
```

-	Layers:
	-	`sha256:c49448d61ad5ced29bd56c68bb954065720d57e32e113f0662c25f7b531b2aca`  
		Last Modified: Wed, 11 Jun 2025 06:38:32 GMT  
		Size: 5.3 MB (5252512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9283da2b6d1ad332bc0b20d88039d2574694be94b98b9ff7d54d8b0b8d185b`  
		Last Modified: Wed, 11 Jun 2025 06:38:33 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
