## `clojure:temurin-26-bookworm`

```console
$ docker pull clojure@sha256:e8f2063d9bde2f8a11778f57af481989cf92d008729f8e82f61b9349ab72ceb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-26-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:08ac30aeeb23fb4dcee89289fbf115c1fe89fd904fe1795428ff0dd207f10d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224227870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75255f389f8dcf7840939a714bf3e3f09fec459d7bdb9acf9d9945ad3de587b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:45 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:35:45 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cacdcc38131b51a9258b2ebc7cc9771ffb773de1989a7edf7003079ded4026`  
		Last Modified: Fri, 15 May 2026 20:36:17 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ebfcbe72f7062c58650452efe6d8b815912bb67998d2613a5f89aa055e59ce`  
		Last Modified: Fri, 15 May 2026 20:37:32 GMT  
		Size: 81.2 MB (81213776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1282fadbde88f0c13a2dedbd27b46832f2c08bf19404c1402662468774c50e4a`  
		Last Modified: Fri, 15 May 2026 20:37:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc77138a321c3a2f2b781824ba97e6bb5b8ab3a57e362fbd2b3096aed128cf0`  
		Last Modified: Fri, 15 May 2026 20:37:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:79aacea361c0b42936a639fe8e673c7ec4fc2f44082d06f13e264e34963580b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7361111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2286dc38ddcbe2506bccbd1128e18906761e2946fb69cd54f4c32bd0bb4ed5d0`

```dockerfile
```

-	Layers:
	-	`sha256:7f9341c0c8abb66b17f6722efe38f552ff94b6258fb2e31da4ac3db05dc54eef`  
		Last Modified: Fri, 15 May 2026 20:37:30 GMT  
		Size: 7.3 MB (7344502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3374e2dba741fd4bd780a112ec202449795f85812732a8d0cc30efd8e48cdd9`  
		Last Modified: Fri, 15 May 2026 20:37:29 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af0c3f36252cdd3464d5f3edc46a4440c9380d4f9f97de529c26b5d90ee60bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223073751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0501ae3926f5853ba56cbda2ffdfbbcb0f53ebd6968fd763d71e24581ccd1c8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:35:57 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:36:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:36:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405bb9216868a405b56cc0634aa51965443ef7c830610334ab92583fa3b7e64`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 93.5 MB (93504390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae4a8503b23c695123c095d546bcd508a5b471629c49cd35690f25ba974bf37`  
		Last Modified: Fri, 15 May 2026 20:37:12 GMT  
		Size: 81.2 MB (81195165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f3ea66d5bfcdae89693d079ef3e79bc536132a89511800797f39fa997afef5`  
		Last Modified: Fri, 15 May 2026 20:37:10 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c758f50105bd817500eb1caf0e306eafa5adbebd413e77d9a7797fd6dac0de`  
		Last Modified: Fri, 15 May 2026 20:37:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c800b64f83c3f9528ed9f3b78402c3924e48c7cc99c9b641aca4f75f4feb1106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bc3dfbff52e4ca13906b3f8ad3659071e55828fb24684d8be5344ad88f4dd4`

```dockerfile
```

-	Layers:
	-	`sha256:470fa66219bf57e2a520b3f13afdf1a542bab9e4fd421ef3f00708d7fba1cfa1`  
		Last Modified: Fri, 15 May 2026 20:37:10 GMT  
		Size: 7.4 MB (7350286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35af591d42b0a0c27830ff5a3c49353fc5a0877993cba36336c9197e1fc9035`  
		Last Modified: Fri, 15 May 2026 20:37:09 GMT  
		Size: 16.8 KB (16751 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0922a64928316de130e956900bbd28dc2aa7247615dd66dec5536b975341afa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233273253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7672f30ec2349c281eafd8b710a253b281b9747e0bfcda77856ec890ba78c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:45:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:45:52 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:49:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:49:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:49:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:49:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:49:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fd299d196bbbb90b619a2efbdb555a0daabbf409ed235c488e800b3c6f94e4`  
		Last Modified: Fri, 15 May 2026 21:47:13 GMT  
		Size: 93.9 MB (93902030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6b607ad84d58cb131272baee994e0556580330b211622b6f5710f93320e8d`  
		Last Modified: Fri, 15 May 2026 21:50:27 GMT  
		Size: 87.0 MB (87033392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a7a42ff96e15689108391f02a26fc20a893b1ae6c570ec98c9ce4d2e679f08`  
		Last Modified: Fri, 15 May 2026 21:50:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c952493f4fc6c7c9777a7346c92b5f36a3a80d24ec456f49941e0fe9d386f9c9`  
		Last Modified: Fri, 15 May 2026 21:50:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a2967a0b618f3917e118611ef012aa5241e362b85407a17c1a46476c51279f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ba129b6628ca21e75610bdcba2f806a03c59640e13c6838aafe9f544d1c32`

```dockerfile
```

-	Layers:
	-	`sha256:4f9fb6a8fd5c696028bf2fdb2f96c6cd753d6fac919dac9d75d524e62b8cdb65`  
		Last Modified: Fri, 15 May 2026 21:50:25 GMT  
		Size: 7.3 MB (7333666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf978136b66883f8d428cf96aeee151b3c0e2eb87f048ab9397e8c5d67dd1e5`  
		Last Modified: Fri, 15 May 2026 21:50:24 GMT  
		Size: 16.7 KB (16668 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:603d6e1b6e4e1aba632da1d8861cb038115977096c6802a0436738714a8764c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217711778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de634ff624e427fe72cfcf646b42578724eabe039a51aa47e7b2d0b1c149076a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:30:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:30:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:30:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:30:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:30:41 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:31:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:31:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:31:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:31:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:31:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3de40ea107fcc269520f0a1c3fb1994e74bcfdb297a866088a152f614bb3e26`  
		Last Modified: Fri, 15 May 2026 21:31:54 GMT  
		Size: 90.5 MB (90536963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6aef82ba8db21a0d362c66fb2a1df8b8d4a710df9f75f87da3c984d1b7275`  
		Last Modified: Fri, 15 May 2026 21:31:54 GMT  
		Size: 80.0 MB (80025748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0dc35c99beecabc565acd237a297d87e826bc95e2a2efb429e3787fbd0d47c`  
		Last Modified: Fri, 15 May 2026 21:31:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6ffdcdd8f3690a569b89d33782a22fa7577c7646a96ba1c2457fd931d9c70`  
		Last Modified: Fri, 15 May 2026 21:31:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e3ae70c667528264e3a4d7c82cd099a541e3bc78d3b67b588e88e985aa395398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ec3971e7da44b1ebd5751b1915db09d51cad4af2196340b25f2b8c59d04efe`

```dockerfile
```

-	Layers:
	-	`sha256:030a0c49aa55e8cd89eedec070b319701261eefb01c800e31021bdf0bc1490fe`  
		Last Modified: Fri, 15 May 2026 21:31:52 GMT  
		Size: 7.3 MB (7321007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7477074bdfa5dd51cd59a4ef24ca505c5a95d940405125919a915ac58cdc88`  
		Last Modified: Fri, 15 May 2026 21:31:52 GMT  
		Size: 16.6 KB (16608 bytes)  
		MIME: application/vnd.in-toto+json
