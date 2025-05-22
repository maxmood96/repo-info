## `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:424342ee4b54a4f4a038d3c7e82d2b936d82ba21b50e8e29176732ba39dafa34
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

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7731d99c4c043575a3ce53ee24ae33c51778e666c92ae2baafed2ffd76aa8430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259114020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e20407602e8304d051c0e64a23138a993584632540d6eadd9d377fe80f518f`
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a890068bf1806a44acb308eed42fc802e900a56e5a5bc157868bf13c7f5a5e53`  
		Last Modified: Wed, 21 May 2025 23:33:33 GMT  
		Size: 157.6 MB (157634458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f831ad471f04071e2883ecc1d82397630ce163c86763142f2d2f49cbdcf77981`  
		Last Modified: Wed, 21 May 2025 23:33:33 GMT  
		Size: 71.7 MB (71723142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd2a97f6c99fc515363834526cafc3ff67e86789f8b8e72d82033d58a860afc`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb49c8c2a982192146be3a76c5e64f3e3d4f4ee23053e3667c58f731ef196cd2`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ffad14eadbd95ff397d267691c817de75b337f44194446587547115932303645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9e7d63500c3bee5822b61dced69a55d3f092b7feed45d133c75d3d25caaf8`

```dockerfile
```

-	Layers:
	-	`sha256:f0d4883434c5d68b479eaec78b737a3ce1bcfd146a2c4a57950fc6621c2ae076`  
		Last Modified: Wed, 21 May 2025 23:33:32 GMT  
		Size: 5.1 MB (5115855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d50b65e977166995ed8269bb4bceeb1f86042f36b11f91c30a022fafd0c361`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5d27ddc491a79e10dfb5fa69542ce86d2d592071c904876938e7bcb6c28f9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257706430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147becddb78f8126b71dc19e74e75c87445dfb308fa7149fa5c33665c99df098`
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
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0151d89edf53b7ee6d783f7001ce04a78ae3663d78e9c1b824dc8cae0849315`  
		Last Modified: Tue, 13 May 2025 18:05:25 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7669214dc8fe5ae10e6b3a4b4fca0d8218c274db2d0cd6df6f59c802e00f5aad`  
		Last Modified: Tue, 13 May 2025 18:07:30 GMT  
		Size: 71.6 MB (71646332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0210c46ad4e8053c0ba5f543bcebbe44e1f6cdef2bfc7d74c5b23bda0dbc0956`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8e768d28ed87dea6d27a23b370dfb67bc3041fbd3b149ce2e6a4a04fcab60c`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3015c8c2c8e184b0bbdb43f4caace8057349cdd20c42150e338c53a836169c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5092955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d19a68587c0a02c777c71ddb24b5308f0d196920c927cd6462dc345ff54e6f`

```dockerfile
```

-	Layers:
	-	`sha256:2d666b701086e09986f6c9c9141c5b957d84a31b09f6e3a5cf782c78506b016a`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 5.1 MB (5076270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ecc3a18fda201cd8a2e63658f61addc291d6f3ad5c3ce981434b2db358cb8b5`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:08e3d2c847d7586fc63275d8d6b7b266d0e4433f9a753b0611f32a80f95e89e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268598625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1c56b4486f9349fe517b17817ac879f7d914aec97980960ed23281bf6b20e8`
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
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b4bcf42e5cf6f5aa92e1672f803cba9978d3d2220c0765df793902e8549a5`  
		Last Modified: Tue, 13 May 2025 19:18:51 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb2923dbf22d99af8d8de790eee35ca093feb46f16d2c03bcb4a4f7a39e8caa`  
		Last Modified: Tue, 13 May 2025 19:28:39 GMT  
		Size: 77.2 MB (77214984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c380bffee672d73280f901548a33aa3ecbd6a27463c01b88a424d3fa12f3fc`  
		Last Modified: Tue, 13 May 2025 19:28:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b3f1d45094466dc91cbb3ad710ed1786de16c534e411de4d31fa1894d3c00b`  
		Last Modified: Tue, 13 May 2025 19:28:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6ff9184819d4b845cf1ad6b8325c83400326af99bedee9d70b7a5fd7ee3e4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23ffb5950f2503e56cec501bf5599c926d9e4b9b8890aeab1bcbf0f8c4d6dda`

```dockerfile
```

-	Layers:
	-	`sha256:481a34b8e0e1eff71df1ffed28e5da69fac82c98c458cb0c9adf926deb14976d`  
		Last Modified: Tue, 13 May 2025 19:28:37 GMT  
		Size: 5.1 MB (5074698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67716a997582787a47a9ba3b3ed84ed9d007060227d75f303c8d8091137cc479`  
		Last Modified: Tue, 13 May 2025 19:28:36 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:d3fdd6f0910afeb3738dfdf70b1730a1dd32d3d645d09c400107eed00db7e1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252387964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e8e7fe5f5d4fbf345860a88474828148c47b398ee573b1625d55e56d6d3721`
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
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Wed, 21 May 2025 22:38:21 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2f883243c7cda03adcd9f44b58b22feb78b4904813045b15aec217a35b4569`  
		Last Modified: Thu, 22 May 2025 00:12:37 GMT  
		Size: 153.4 MB (153449674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211b59c743c18d7c70a1841112e481c8d25254f4860a3824b7ffdff0451f06d7`  
		Last Modified: Thu, 22 May 2025 00:33:20 GMT  
		Size: 70.7 MB (70691895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e6a238d72f702b7814b9af39a305f680868e61f583569514fb90d1fc2b0969`  
		Last Modified: Thu, 22 May 2025 00:33:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b681e94ebd030478d45411cd00f28bef75dabd0358131dbd2a365d64083c4109`  
		Last Modified: Thu, 22 May 2025 00:33:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7264862233caad25fd46848868eb7324a50db71888cdd4861243bd732c336b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0322a570c1e9069c32f4b2bcb7ce1614d83a9ddfdf61386e13d4a8f2180b60`

```dockerfile
```

-	Layers:
	-	`sha256:4d9d285c583417b1386ace9c7277373a9d126339c82fb40a22a39e06873cef4c`  
		Last Modified: Thu, 22 May 2025 00:33:11 GMT  
		Size: 5.1 MB (5105331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b9bed869b33f17560bc373b95d1dbf91a1821cc2754d5c66231a5eb3d5960d`  
		Last Modified: Thu, 22 May 2025 00:33:10 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5ee1328d505eaa9de103096a22d89d6b350947769faf22b719f12572ba2e0b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249553602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec044c8054f8692f943d8f879893d1a586abd86f2288e7415c906de48dd295fc`
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
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4125f64ccd594bf8ca4128edd7e99193b6d38e00c6963505c94cc81277b3aa35`  
		Last Modified: Thu, 22 May 2025 04:00:23 GMT  
		Size: 146.9 MB (146910924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50640d5e0d9a4b2b4f7174692fac48c09829ccf4b854eade44b6fad9a0d446dc`  
		Last Modified: Thu, 22 May 2025 04:04:46 GMT  
		Size: 72.8 MB (72812020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a173cf5b9672deb9fd35a939632f35625debe8d5f2dc0f40f84ae98e9ff12`  
		Last Modified: Thu, 22 May 2025 04:04:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666cf274f2200710863d7c8f8ae8889709398e5ec2825caae1d5844125b8de26`  
		Last Modified: Thu, 22 May 2025 04:04:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e026121d05ff7c4cd7bd003c48a779145abca444936c12e41b37ee36dde08f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a93454ae8274aa61438d0d91ed900b5c0f05c7e8959a0cdfa3dd3e7a82f55e9`

```dockerfile
```

-	Layers:
	-	`sha256:07ebdb35b2192df529f4e1b26088ccee7ae363cb36e6a54c990568bcabf5ca39`  
		Last Modified: Thu, 22 May 2025 04:04:45 GMT  
		Size: 5.1 MB (5111779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025154fb823fbd8d4aa5f6b1f5f92b40241c345ab94ef3af3d999210eb7cc245`  
		Last Modified: Thu, 22 May 2025 04:04:44 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
