## `clojure:tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:f199d87792b295ea18bb5aa6a19d12bc715392b1cf845e7e397f6b4176825f5a
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

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3ae1d1918d8c3abc75445d5a7ecd170640068a7b6c2177c286df9e26091434c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259113372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13005b99416154850aff6cce79634011d790ba002b0aef621f865ddbfa27370e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Thu, 08 May 2025 17:06:40 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442087327e103058d05d468d3f4ca801a98c2125c72af762dd5505946f3a6b4`  
		Last Modified: Sat, 17 May 2025 12:54:02 GMT  
		Size: 157.6 MB (157634443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c715d6c5c2be2cd2978bc378410277a9436e43a98682757be199c183476de5`  
		Last Modified: Sat, 17 May 2025 12:53:57 GMT  
		Size: 71.7 MB (71723975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330889c77699fd163694fe39a941fc372f8ed8487bc4240c67f14825ebb536e4`  
		Last Modified: Sat, 17 May 2025 12:53:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb92f5f477f1e3e8b51331fd3d58d5de8df0b7cc02d5b00d41208407da673e46`  
		Last Modified: Sat, 17 May 2025 12:53:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3cddbf4349291a43c7d659ea634457249a4927c4c07a87c793eebb90f5fc640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b124dc9923750c77f74980c1cef27edc9a75c9dbe4a068ad2603260f6bf6cf78`

```dockerfile
```

-	Layers:
	-	`sha256:83aa6ca87948f797541b5f6e8ed2c87ced73afd398d4d79d29b411a240f9b73d`  
		Last Modified: Tue, 13 May 2025 17:54:12 GMT  
		Size: 5.1 MB (5070477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef6b821ad4dff3e5b3b478342c162df60fe9b9b06604afe7f7f349c88b0295e`  
		Last Modified: Tue, 13 May 2025 17:54:12 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

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
		Last Modified: Thu, 08 May 2025 17:31:22 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0151d89edf53b7ee6d783f7001ce04a78ae3663d78e9c1b824dc8cae0849315`  
		Last Modified: Tue, 13 May 2025 18:05:25 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

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
		Last Modified: Fri, 09 May 2025 00:17:30 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b4bcf42e5cf6f5aa92e1672f803cba9978d3d2220c0765df793902e8549a5`  
		Last Modified: Tue, 13 May 2025 19:18:51 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e3207b3d91ddb0be688a79df548d0c36db9196b9249a143f26c5d9ddeb0cf537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252393852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262aad48465830ffe08e872e543b6c7f0d0221549d5ede0c7dfefaa05e3929d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
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
	-	`sha256:facf81ceeaa2f81a0f9ef1ab66d52f94aba08977754588b2609aaf3106342525`  
		Last Modified: Fri, 09 May 2025 06:41:03 GMT  
		Size: 28.3 MB (28251718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb996ead12e059ebd9c7e8c86c157e34856d1e147455d5106c6cfd234b1d54c`  
		Last Modified: Tue, 13 May 2025 18:59:41 GMT  
		Size: 153.4 MB (153449662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54a7cf32b179c9b937246536e8e46206967f835184536452f89267817d232a`  
		Last Modified: Tue, 13 May 2025 19:22:20 GMT  
		Size: 70.7 MB (70691434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b584ceaa6c9abc20fee74d5f45b5f73504453b18c2522bee9899274190f8d474`  
		Last Modified: Tue, 13 May 2025 19:22:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d326a597ba1f2602023b1d03818ee007aa3ce107591d630b636b386037dde25e`  
		Last Modified: Tue, 13 May 2025 19:22:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c44548568e63a274bd9b0d855d8aa1afb0fdeaed65f3ad06dd68360620b9f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de3a17f10bafcf5d9643cb9ac33cd918e4659dc9fd07315f0fbbb3bd32e07e2`

```dockerfile
```

-	Layers:
	-	`sha256:ff8503fd57865afdba3a8032179b70b3a8e76ea4b8c088a99f4c77a758322b84`  
		Last Modified: Tue, 13 May 2025 19:22:10 GMT  
		Size: 5.1 MB (5060071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a5659a7789ac769f7a665eea252b7b62b6e947bc8b0cf62c5a7bc863cc8442`  
		Last Modified: Tue, 13 May 2025 19:22:09 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fb191285cfd0256b35fc485c76c838afa6aaf2ab5269075a66c78e37354aee43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249550322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3d939759b3742ae1594485ce606f1818f6ec21ac392152b7560783c56d00b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
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
	-	`sha256:2efa8ce97d282fc76ea2985fc31102becef655447ddbf9bdd3209771347a0182`  
		Last Modified: Thu, 08 May 2025 17:32:36 GMT  
		Size: 29.8 MB (29825462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc96bb5e63b39bd319b29b6e426b4ceeb915fd8f4169a26811de8eaadd5b4ed`  
		Last Modified: Tue, 13 May 2025 18:26:29 GMT  
		Size: 146.9 MB (146910892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6832adee761961a5cf37afb9636547fd83edc20d47e59ad096ac63fc1b71ec96`  
		Last Modified: Tue, 13 May 2025 18:32:34 GMT  
		Size: 72.8 MB (72812928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6f5a9002ec87cf66e40e90eb7e8c4011eb04ff55146b58531d55987cbbb0a0`  
		Last Modified: Tue, 13 May 2025 18:32:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f5897569defede1761fbd2f561fdc000123f418b60bff96a6a1406f27b2fc`  
		Last Modified: Tue, 13 May 2025 18:32:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e88a8b1f8a21ad443790dca7f660144c434a1b17e99d703725de6bba2427ce34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd817c144ae519b8d2242e17f85eb2454e7bda77045aac0b4150e2c4f0eba326`

```dockerfile
```

-	Layers:
	-	`sha256:0fcc19e333b3386b4deba20cc564cfd06b7bd0b2aba91f748f5215abc77fd25a`  
		Last Modified: Tue, 13 May 2025 18:32:33 GMT  
		Size: 5.1 MB (5066401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d4d5fee9ef995826689b8d2ea3d162e14afd6e1b019ec8e30edc21021452123`  
		Last Modified: Tue, 13 May 2025 18:32:33 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
