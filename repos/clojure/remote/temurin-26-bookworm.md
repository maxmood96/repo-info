## `clojure:temurin-26-bookworm`

```console
$ docker pull clojure@sha256:1924ae8360e747b87167fefa22fb0e061f94cb511a691b36c87e3bd58d5de648
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
$ docker pull clojure@sha256:2a8912d82bd5527cd68193ddcb3e3d83c68f8a3f2c5e45ebec8957dba6459ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224233515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dd71c77241b28d6dd9bcb668a799d9cc91962fdef92f9614e987852459df63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:17 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:02:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:02:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a49998aec6b2dfbf350d5124f25cfa4b7f7cdcd1fd78a2c358a9c0f1ea27fe9`  
		Last Modified: Wed, 20 May 2026 00:02:56 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301f8419e84be164242ecb71bc5abf9c4ac51c17340184a9983488e305d955e8`  
		Last Modified: Wed, 20 May 2026 00:02:56 GMT  
		Size: 81.2 MB (81212701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c801a9a45a630925dfe8a78f59629ab0f856e958aad54327b3d5fa70d8aec313`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9825abfd115287f7b1615aa6c55912abcb96e7de43e5f6130e6f0b6a7e8cad4c`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c17ea380dacb75a884bf6c5de058cfe575f1315cc685bfde7ca09734ea322028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7361133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5e313dea80ec0b3c01b96e1c2b8890592985add812a99784d9233203eefe7`

```dockerfile
```

-	Layers:
	-	`sha256:e477cfca1308f1a113040b6d63a78bdc174fd7584a5e89da30c74310e76abfd6`  
		Last Modified: Wed, 20 May 2026 00:02:53 GMT  
		Size: 7.3 MB (7344524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b389bd71f1e26c5ba76f775ab96120915f1a5fdb8666f60df3af9c6ecf36a97`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3dfbff2624e5ab99474c2d0ca8d99c154d95652a9cc040924dbc3ac0ddeaa0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223098446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4041a1eabc788474b1b4412b9a04bcadf0724c8c980f08de4cc4fc140e39be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:09:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:01 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0336c35f973a9813043cc07ecc68d7b9451d2785d0126e459a1289829b406`  
		Last Modified: Wed, 20 May 2026 00:09:39 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d957823114ed7d51944d808bb829919b37e4c517bc34014e814ae7e23c2c1d3`  
		Last Modified: Wed, 20 May 2026 00:09:38 GMT  
		Size: 81.2 MB (81213624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ed67fc38028691506356d8846a50415d82dba076e4e278d458d2ad8ec1f99e`  
		Last Modified: Wed, 20 May 2026 00:09:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8c9eb5ff49008593d68012c8e0b32aeded44c876e0ba8739fbbde899525609`  
		Last Modified: Wed, 20 May 2026 00:09:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4910f1dbf19aa596124f3065168ef5fb5d9c51500500b5e42231ec8a9ad9e24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2209e12bc1c2208061831c5b14e86754045c9c00fcb1e1b12ba6b8b161dc8f3`

```dockerfile
```

-	Layers:
	-	`sha256:b23b5c4f2486649bf8b14f6686cf23b24f08824f4f73554986dd267458a72769`  
		Last Modified: Wed, 20 May 2026 00:09:35 GMT  
		Size: 7.4 MB (7350308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd0c7e7feec5ddaef3983c1c5fb1f303243e3c1dca9f59a8dd0904a64c9ea4d`  
		Last Modified: Wed, 20 May 2026 00:09:34 GMT  
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
