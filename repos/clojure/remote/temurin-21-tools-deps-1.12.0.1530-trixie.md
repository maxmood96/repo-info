## `clojure:temurin-21-tools-deps-1.12.0.1530-trixie`

```console
$ docker pull clojure@sha256:cd7fd0681e21a82de96138c77fef18e7559c8d20ce7931e4929983ca635b80a6
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

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:65f4c1df28f271390e7740c4e50b6c8149d2c10192f0e7a454254f622f432df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292141365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf352d2f82479cd43255a6d49ec1dbf0f6a598afcee338aa8f8d14ccdc07c8a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168e8eb82c2b6143dd8c29d4f14264b3669c63153f1e2f0832ccd6ef2a2ffc7`  
		Last Modified: Wed, 21 May 2025 23:34:10 GMT  
		Size: 157.6 MB (157634458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f8ea2a1d688e401231f7ad84f0bbf6e18a293b9ab6fa010a8bf0088601c3b9`  
		Last Modified: Wed, 21 May 2025 23:34:09 GMT  
		Size: 85.3 MB (85258959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c1f7f0748ad6e828832426d7563751effd912e4e01f09a302b4f0ca3f83de0`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ff9309b76ef3e1229b299689f5cdb04f290c6cb8da934258f814beb18f1d55`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c7a1485156ddc0f48a61b661b9413f01f31d860b695daca2ca46c4cf9e41d242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e59226e99595e9b72cfd691e158c1d62cb7da3f341a8851b463fdcd9e9d3995`

```dockerfile
```

-	Layers:
	-	`sha256:56a947085a4f1c5a3f471b621a604fb5200a2d7081be59e34dcdffd6f7c15c78`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 7.3 MB (7322186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ea97711809240ec5839d4da8eb890c2000d3f0c55ed65a199d1dbc8b1aba7a`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af12fbb841e51b97c5dbae42a999457484829eb5ade8fd3547c9693658bd8737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290726422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b02d5e8bc5806c52d8cc468a7f05d82f93e64f750496e2c01c7e7eae3616bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676c3e417baafaf8b730adc6d0f78dc3fa5bdbb2f54632cf85169f85047e3825`  
		Last Modified: Tue, 13 May 2025 18:04:24 GMT  
		Size: 155.9 MB (155928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1a01c6ad14d6ff0ffa6af0dc5d67dddc139e939d67b6e2723672993ab8debe`  
		Last Modified: Tue, 13 May 2025 18:06:37 GMT  
		Size: 85.2 MB (85172457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f9716b24e7995becaf5b62afd017d09ac2c1ed1ce9599acab5cd405cdc6b88`  
		Last Modified: Tue, 13 May 2025 18:06:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769dd8d09e972edacf7d5e6219f401b4ff4aa0ce935d1fbea7e00886cbfe7cc`  
		Last Modified: Tue, 13 May 2025 18:06:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:26fa8e7b45ace23d6e48b2e93fcdec2c550fefad929b6368a7165ba263dc053a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7296600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b311074def9ebbd6bd231d961cac5da839534ae84799fcffd75025f5d3667e16`

```dockerfile
```

-	Layers:
	-	`sha256:6552a24acd51053818384e1a34d1100ad89af33906624b6f068242659ec6b337`  
		Last Modified: Tue, 13 May 2025 18:06:35 GMT  
		Size: 7.3 MB (7279993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0304755cf1ff133a54a6bea45ab41a2da880ac70dce8e8552e0167da932a67`  
		Last Modified: Tue, 13 May 2025 18:06:34 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a34dd8bf13f7e9c772a35f54904c2886132fcc77db202081988bbe382c5ab431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301620828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46dbc7ddc5a3a931481b096b8d79dac8ab5b6f0cc76661787e0b2dfd53acc230`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2151ad68f58c4cb07dda1a2a4084ab06210fce8cc616b99b367a4f681d8b98`  
		Last Modified: Tue, 13 May 2025 19:16:46 GMT  
		Size: 157.8 MB (157804906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1244fd0b92cb79324efdaa7304cfcc972af6d966e2471b0e29408c459ac6b0e7`  
		Last Modified: Tue, 13 May 2025 19:26:57 GMT  
		Size: 90.7 MB (90742325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4ac494317edb5eb108af357379841999f38c9bce66303830167250c0bdb4a5`  
		Last Modified: Tue, 13 May 2025 19:26:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01e012d6bece5b94a3191bcc4fa5a311c766c4cd3ad0bac52e6267dae42ce5`  
		Last Modified: Tue, 13 May 2025 19:26:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:856067f5af8c5826624563b16256da23b91bb2ff48e1e739a00c0424ed54c39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7293729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912f8c37ed31e80bbb751e8861d74153a835879200a4e6b3097ab64eb167c85b`

```dockerfile
```

-	Layers:
	-	`sha256:76efd912286cb10604e3cbceee249017004455d08875c21bcc129c716fea52d8`  
		Last Modified: Tue, 13 May 2025 19:26:55 GMT  
		Size: 7.3 MB (7277204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e221162ac93f6c3654273781c4f11a473e74145cb6f0d9247aec188e642448e`  
		Last Modified: Tue, 13 May 2025 19:26:54 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e9c784a759c8daf6231d02060a9b472abec4d588b7d6861d3ab1eb364183d883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285402736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd69b0496724e17c88ee122d4ce48119d18f1e255d8b1352e41a15f4a4a38d4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe8ec02123e21854915b01d6677a1c1a15c0937fd2d1cface7f9a608d2b0082`  
		Last Modified: Thu, 22 May 2025 00:04:54 GMT  
		Size: 153.4 MB (153449647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff2c4eba794e6381ac550d754b7aaaddff388374f8993dbd01241f03c6a5192`  
		Last Modified: Thu, 22 May 2025 01:27:41 GMT  
		Size: 84.2 MB (84220635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc880de66157dc76063dabf00087f1c59f970e90121f3e4ce4d95c6773b9a6`  
		Last Modified: Thu, 22 May 2025 01:27:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ca7e4703521885353bc70ef7c42c72818904da326f2bd1bbaa9609b0179b14`  
		Last Modified: Thu, 22 May 2025 01:27:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:07a7de4ec177a8fdda120097ebb1b14bd156d3f0db687c897dcd32eac426b330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e54f4a2e855681a2b12f3a477ca12e509f642f1d7993971ca9e93bb38c45834`

```dockerfile
```

-	Layers:
	-	`sha256:17c45b82c025445100315c98f9608e2702662c0d3f56775a5801a9ca4850b39c`  
		Last Modified: Thu, 22 May 2025 01:27:31 GMT  
		Size: 7.3 MB (7310109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c299d15f31a5c70b62064c993056b80473b4ed4eb641bae01a02f5bab867976`  
		Last Modified: Thu, 22 May 2025 01:27:30 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:33e40a0a3c809bd8e0c5cec9eb556d5da2545b7b250fbd00e9ddeed1037be4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282574439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2953eca9ee57bc972ed866cbad5720a8e2f14ad32805f9aec38bdabce0dbc2a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca90e1686a05daf35be5cad5eb0988f39b9f2dbcfbee3671b2e5fa86bc4f79`  
		Last Modified: Thu, 22 May 2025 03:59:19 GMT  
		Size: 146.9 MB (146910920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb774c4f7067c9c383c1612b73422ed297c37a90cc3aaa1d7c3b3dec575eec99`  
		Last Modified: Thu, 22 May 2025 04:03:43 GMT  
		Size: 86.3 MB (86340248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c837153dee173c2baaf094e402d935f16ed8882e70e81ef2d131690e112f87fe`  
		Last Modified: Thu, 22 May 2025 04:03:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ce9bff36189435de3e324cef8ab7e431e34b43d0abcd3504ba169e7d9517a6`  
		Last Modified: Thu, 22 May 2025 04:03:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:918990a5ae0f943ffcead01d5c54475390ab4ea856fcdaadc3e15e28a8459f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e61688951995becf4da3f0d09e7e805589101a6743565dca5cc79f7be5cab6a`

```dockerfile
```

-	Layers:
	-	`sha256:1b39fb88fbbc142f742f3ad3bcf7fb339c853d3accceb0fe5ad25ee9f61f0d1a`  
		Last Modified: Thu, 22 May 2025 04:03:42 GMT  
		Size: 7.3 MB (7318108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af2b2f09672000b48d79dcd7cc60039e2e3d20202181ca389313e7ec5bfa2f8`  
		Last Modified: Thu, 22 May 2025 04:03:41 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
