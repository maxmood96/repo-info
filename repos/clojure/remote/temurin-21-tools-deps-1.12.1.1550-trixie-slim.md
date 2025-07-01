## `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:65374de7185026b78c5758f7835f300aa3b52b1c782aaacd022ab00db0f29df5
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:478b23e632625a7406e630ff51fa9b8e935ad4afaa81a00538c3148e6a705219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259208491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b40383861a859d22640acc52b2762cd0bdbff3631337a5262e3fa224710d576`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa7d4d69bb1662340c2ed06dd63a27c79e754a7eb1446fdde8f1c96de05b719`  
		Last Modified: Tue, 01 Jul 2025 02:41:09 GMT  
		Size: 157.6 MB (157634485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b3f22c2aff5d8cbfbc910fda7067065e05f32cf21f559d60088ecaa82474e7`  
		Last Modified: Tue, 01 Jul 2025 02:41:08 GMT  
		Size: 71.8 MB (71811859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef197231886b03140d08453ec55257b84c0f59f495093954ea405e70ebe5b25`  
		Last Modified: Tue, 01 Jul 2025 03:58:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b4945aa7117d2c254750dcf44d8e9c4bdffba60605716b06c69d9bd71de24e`  
		Last Modified: Tue, 01 Jul 2025 03:58:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bedc8edf58bcc695d3191db590b57e4f5367d53385c2d2166d728baed7624446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294ee238acf139c6201dce79edc5831f378496f577c36d03352ee5837f9e1477`

```dockerfile
```

-	Layers:
	-	`sha256:a144da80fa6b9b5c8df2fe32f39fc791e95c3aa6cc7ec3e4fe56928c3d11299a`  
		Last Modified: Tue, 01 Jul 2025 06:39:53 GMT  
		Size: 5.3 MB (5256592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e726ce52ef890fd2c9a7042c9a7453648aed8f78019caeeceda6efe4006ef9c`  
		Last Modified: Tue, 01 Jul 2025 06:39:54 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

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
		Last Modified: Fri, 13 Jun 2025 17:25:55 GMT  
		Size: 155.9 MB (155928799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134f08795483c836143dee8cedafc23f7029970a0f92e73bbc8d0ad8aef6b291`  
		Last Modified: Wed, 11 Jun 2025 12:21:18 GMT  
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

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
		Last Modified: Wed, 11 Jun 2025 12:19:08 GMT  
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:70b1a7043b7cf4c72ddfe6413b5fe7e16142aee6c34c7ceacfeb5d37ba5f098d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252413181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7888e3aa7ccc71a1215df6a48b29a39c46db9fa96710ecdf42cdcd7b1d8fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8616f7bedb56894be7fe53d122ffb03b37e9993aa4c114656ea59dd01cb38176`  
		Last Modified: Tue, 01 Jul 2025 03:10:02 GMT  
		Size: 153.4 MB (153449650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af318ab6a70500e9f73e09addf22a7ee42a01065a08d029534a1d7116e26517b`  
		Last Modified: Tue, 01 Jul 2025 03:25:15 GMT  
		Size: 70.7 MB (70703521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7559d357ed5b8676e56512a4bee290f27190afb11f0e2ea7a4c9ab9adb65bf4a`  
		Last Modified: Tue, 01 Jul 2025 03:24:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ecc037f824488fad2fc66ef59b36689e8b95302419172b397631f0062ca2d3`  
		Last Modified: Tue, 01 Jul 2025 03:24:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59435b20bfadbc4f22084fc8b672f97afb1628957761a3bae6cd518721ed1d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cb65f0944d1cd0143fceb6f4f914ac0ddb1425affc0da6833f0e0376738737`

```dockerfile
```

-	Layers:
	-	`sha256:5f1505d1f62341f4800b88c82429be5330fa481b22a6ab56fe9c4507e0a1e63b`  
		Last Modified: Tue, 01 Jul 2025 06:40:11 GMT  
		Size: 5.2 MB (5246068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee36271a7d0a5d62557d71cf8262d2b24d0ed07631786c2c17bfa30d65a5e2a`  
		Last Modified: Tue, 01 Jul 2025 06:40:12 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - linux; s390x

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

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
