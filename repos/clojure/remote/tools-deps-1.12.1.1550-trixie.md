## `clojure:tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:8031602e2446569b984469476f3f8f1bbea1e3f2bb3130a0b1f243cc9e768a69
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

### `clojure:tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1616ed7e9e82854346917ed3de67ac1bad17275cebda3fee346dbe075bbef7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292254194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91884fadc6df27a66cd6331604c36ba3f14ab9c80cafccab77d5be4f5d80a6bb`
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bca81dcca9ef0c568b34450164c1191ee77c1488205ba6e445c97e61dcd3a6c`  
		Last Modified: Wed, 02 Jul 2025 07:12:37 GMT  
		Size: 157.6 MB (157634482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f187e4a4b1b37352de6d7225dc8faf80d203f99a461595b8f80ee1a1054b45`  
		Last Modified: Wed, 02 Jul 2025 04:49:49 GMT  
		Size: 85.4 MB (85354795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff029ae22ce67e932569c15f0ef3d8dc9d852d3c26bd96f9d1d65057b85b935`  
		Last Modified: Wed, 02 Jul 2025 04:49:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0575a8164dfe6b1b65eaaf13f403a8c9c07830f646114994c30e7245fa0e0609`  
		Last Modified: Wed, 02 Jul 2025 04:49:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:024a9a303a5ddbcd8f6546b45ed7ff682fe4226d316f696fac33240b7544b47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db83ea08241131aecf491c89d6a5480dd8b3af7a4e3199d4bd6a5ef642b6a7ef`

```dockerfile
```

-	Layers:
	-	`sha256:000e4f2bdd969edba3d63c002046cc729594e567ad2ae2ff8b41f11bef38b561`  
		Last Modified: Wed, 02 Jul 2025 06:40:32 GMT  
		Size: 7.5 MB (7462923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f962cd50a047639f1f351e683f36b6e9342a8f643086f5c84e9c8c26b58e065e`  
		Last Modified: Wed, 02 Jul 2025 06:40:33 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0575286078e103e9ce2b132c1b8487bc1118cd18f55735671e1e72514281d063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290732404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393d552d5b0291c8762f2e82646567fc4bc152d88987b6318bcea2c44c60bb9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c102048348f860ce1e85405e32ca456a52a441757b642ead74c7b79f92ea6f5c`  
		Last Modified: Wed, 02 Jul 2025 15:51:56 GMT  
		Size: 155.9 MB (155928830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec37dfbbfa628da2742276e0c04906334e449a57c46e7df9c4349fb92a2e46fd`  
		Last Modified: Wed, 02 Jul 2025 12:53:29 GMT  
		Size: 85.2 MB (85172378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8e4c44a302d9d237846ad72e8e6bc253c28b4866c51e1303445ab0942a77f5`  
		Last Modified: Wed, 02 Jul 2025 12:53:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7a7bb5475f1b68a8fe2da9f263d66a98530ea203fec6cbddd56a6658dbf0b8`  
		Last Modified: Wed, 02 Jul 2025 12:53:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:258e7ed597c4aaf6336abeddeaf6c5e852faa99e20cccd19da6ce32480571edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9736bf25447fa3a12a759ec6116169ee772e647939fef2707f1cf00d5a32418`

```dockerfile
```

-	Layers:
	-	`sha256:2deef8b286fcb0cb37712b0022751bba82c6c63554b61650b9354cd98107c439`  
		Last Modified: Wed, 02 Jul 2025 15:41:12 GMT  
		Size: 7.5 MB (7469977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bda7fa1c2df69b76ffb23f46027bdd3fdf3a25f45a2caf2bcd27ede84b92eff`  
		Last Modified: Wed, 02 Jul 2025 15:41:13 GMT  
		Size: 16.6 KB (16605 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ba8163c4e5aeaccf8680875f66ed89fd94e2653c369a40270c9d528543084b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d557eee274a9788cca07ccd5e275e4dd693591e61db268530b49cc53b21be65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ba674ba1404593b1a6a59d0974b4549e6f5655bdfdb982e660021a4e42c0fe`  
		Last Modified: Wed, 02 Jul 2025 10:49:42 GMT  
		Size: 157.8 MB (157804888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad7357907b27562b081acd2e11111b0339cb77938fcc5504f9a0593b8d22533`  
		Last Modified: Wed, 02 Jul 2025 13:58:12 GMT  
		Size: 90.8 MB (90769233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f701bea643d59d8642af5e50b0da29265b2a047a460d4020c4de6867fe4f4c5`  
		Last Modified: Wed, 02 Jul 2025 13:58:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d78a487487c469569d42b4de057d50171bd1448c65d30927811c9764066ad85`  
		Last Modified: Wed, 02 Jul 2025 13:58:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:46c89aa744fdfe10429ca281eeaf91be1dbacb8e9ece80caa0404372fd7e89f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fe4a3739c3b942d4f314595207926636aabf5c4a9dca626ee236e9c9bf86d9`

```dockerfile
```

-	Layers:
	-	`sha256:0cb30828789c1a3a8f64b32fbb62202056edf0c23d1f12a30f2e791e3774b9cb`  
		Last Modified: Wed, 02 Jul 2025 15:41:20 GMT  
		Size: 7.5 MB (7467352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee162f0fc5879982ac5a0d099b24a532c4986f61c627b0dabe0591ee5f6f1d71`  
		Last Modified: Wed, 02 Jul 2025 15:41:21 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e4bfee5602cf185661b87dac0e388b4e0dac75abd0636925cc05d2e30ab648ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285438588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0c7cbd0d12aa7d103ca4801a3f635dc52128fd89c50f50622e37c34d96fe65`
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
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e076e085e4924513404df674a4b5cdd11b691d0a99549b6d4e3c46e86877f1`  
		Last Modified: Tue, 01 Jul 2025 03:02:40 GMT  
		Size: 153.4 MB (153449649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e031c8c36ce5ae72ae17b82b20d3b8c893dc9818b08e07cb8c2e96db91429a25`  
		Last Modified: Tue, 01 Jul 2025 03:17:44 GMT  
		Size: 84.2 MB (84237742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf65a88e6e3882ea20858b7f9d17cad52ba6c9f3bd3503b4bf5b856d18461a6`  
		Last Modified: Tue, 01 Jul 2025 03:17:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d45837c9073667b247badd62c98343241d142c3f8e9bd897a5d8fe9ae1a3f2`  
		Last Modified: Wed, 02 Jul 2025 09:17:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e73b3f94f5053bc35a083d624e2a5dc82b0b1937a04f366e99b07c77dd041ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7467371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f7cea1999f56445d6bdc088674f1f6c927988f1292c25713cad0c3c05037dd`

```dockerfile
```

-	Layers:
	-	`sha256:36a920ed863e5a8bed10792b229161324cd795b5e958e4f10d3f1d54ac63eacc`  
		Last Modified: Wed, 02 Jul 2025 12:39:56 GMT  
		Size: 7.5 MB (7450846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de70761faef6b194e4afdf1b2ae288f9c63bfb5d712b2b3db5c59512c9cb8efa`  
		Last Modified: Wed, 02 Jul 2025 12:39:56 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:09306bbbeabbaeb9b1041231e4d55634908fb1952c0bd37b8155c3a22504c55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282590427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227b7245beb5e4cceb39fa849c96837a73723ad11d658e89cb9fc2c9d4fbc2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bc60726a2f3745d54c0dd09294d4451be8392d24b90a4488a0071b6ed0b78a`  
		Last Modified: Wed, 02 Jul 2025 06:48:19 GMT  
		Size: 146.9 MB (146910935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7bffe859bd89a61a9c2516b34aaf56b53d4a16877f8d27a33f2953516f9ed5`  
		Last Modified: Wed, 02 Jul 2025 06:54:04 GMT  
		Size: 86.3 MB (86334792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21867e9837efd16da219eb60a700722b7d20c7b0a6e64acfbbace178168f6bad`  
		Last Modified: Wed, 02 Jul 2025 06:53:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d7fac79b09becea393d3fc379946f08297e1a0654036d20adcb64cc60dab5`  
		Last Modified: Wed, 02 Jul 2025 06:53:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2e7ef8fc102fd2b337bfbcfc42c320e9a294834d1bc45141114ad3449469b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7475310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a1d3f62183359626c5bc3516798d78dd23a429a91004457d6021b03f590469`

```dockerfile
```

-	Layers:
	-	`sha256:1f0ce95a478af19b5bbf2eb0a237c3ec06062d384bfde9e45bfdd854ebb74fa3`  
		Last Modified: Wed, 02 Jul 2025 09:40:11 GMT  
		Size: 7.5 MB (7458845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf6fe8c8d745c07205e2b0738406bdb3aabc5d999f7a66843a54fefb14ca70a`  
		Last Modified: Wed, 02 Jul 2025 09:40:12 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
