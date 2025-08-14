## `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:818e4f373859dd562e80bf269a536ee5f53161b475c4f2e2d95e2fbbfd3acc8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:36b469f7e20ae8c3ed3e0e617160635c493cdb0788ef591f64a3b06dc77df54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179237910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660cc29a0726f9619acfbf98b773a5f8f22601f56bb4ab26440adbc4f6edfc57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e087d8cf453ee14a84122c366da6cb37eab6d898c9aa9a5a4d357be9c121c5ee`  
		Last Modified: Tue, 12 Aug 2025 22:36:10 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5124645cee57bc19fd95132d4b82f98e66e62c24e922146cf284c7a4f6af8ccc`  
		Last Modified: Tue, 12 Aug 2025 22:36:05 GMT  
		Size: 59.0 MB (59005520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa56171888a699965f962f5b897dda250f5edbc38cb23ea89978164dacb37745`  
		Last Modified: Tue, 12 Aug 2025 22:35:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85784cd893778fb4920d19a868cd47c120d22aef4ccd289dea57afd545205b7`  
		Last Modified: Tue, 12 Aug 2025 22:35:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1698c7c9e894c577c8f686e3589804ee90a648558a637c33a7974005e5e0604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8166c77eb68436b441a89636370240458232e7cdd538b89cb389c88ad136fe7b`

```dockerfile
```

-	Layers:
	-	`sha256:a5178bfe7a7c222d291373431bd4df189a6e542980f97111f6fcd164526fe4aa`  
		Last Modified: Wed, 13 Aug 2025 00:40:02 GMT  
		Size: 5.3 MB (5258686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458229a7c83036d56c366d42846b46fd35f65027a94d277fb0e8f232e4c79d6b`  
		Last Modified: Wed, 13 Aug 2025 00:40:03 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4dd9e5d2983f9c174817c2ad116b80e5594ab77def4c490aaf649ab4f1f73573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176981735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b59a495d5756181619fd57265071c7772f029dd4c49a0059ec5c2ffe877e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c1ecf514b7389968a6fcc598f3576b4054314f86f720c7eba1c112b4258ae`  
		Last Modified: Thu, 14 Aug 2025 16:15:19 GMT  
		Size: 89.1 MB (89092517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e0d5e7eab84ee77a2127c673b7f19cc65c3f30740754a2525f9ca26ecabd4c`  
		Last Modified: Wed, 13 Aug 2025 14:48:18 GMT  
		Size: 59.1 MB (59137685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f51b1096f8b65327eaa1b4c48eca50abd3f7f39f2339f7a90626759bbd76df`  
		Last Modified: Wed, 13 Aug 2025 15:29:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03279ec27da9524c83f1a6bfee8ad7a749ba2f41c7947e4a8a2670fc16f6a701`  
		Last Modified: Wed, 13 Aug 2025 15:29:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8019de0ad131b90b6b440dc5f95e3da7134f85f1bf724cd363245f8e95447041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9168c85c18e769b8c9d4caef375f2b0f33dda40a8d381a0b99db44cad7033bc`

```dockerfile
```

-	Layers:
	-	`sha256:7a988f1f045dd9d5190bbd24122fcc5ef144f181f6404197ee05ccde5909f78a`  
		Last Modified: Wed, 13 Aug 2025 15:40:32 GMT  
		Size: 5.3 MB (5264415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02219dff6961333839801c660e34aad659070ffc9deabe0d5f596672f0b67294`  
		Last Modified: Wed, 13 Aug 2025 15:40:32 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
