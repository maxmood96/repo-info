## `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim`

```console
$ docker pull clojure@sha256:c6be7220b3a7e58843e12d8865dd5d87ab203dd7b1c705c9859e7216ac677900
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

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f4eb7421133252cc0658dcdaaa2acbcd75f99384aa032a6003f01af35fb81912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256134459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067783b89b3dda867addb0280cdafd14129385c2e5ff44ec168b1c376e93ab65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:15:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:21 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:21 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd5db6ba7f429e2967cc7b246f50b265a2ae5fcaedb918ba89821bef097f5e`  
		Last Modified: Fri, 15 May 2026 20:15:58 GMT  
		Size: 158.2 MB (158166943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a165be5cc05104f86335b66d287003488eaafb9c07cb577b6606a4dd4ac19bcf`  
		Last Modified: Fri, 15 May 2026 20:15:56 GMT  
		Size: 69.7 MB (69730190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13892780f040e9a8f6c58615953ef9769deb30c6dae71040de6171b7ee9d6ef`  
		Last Modified: Fri, 15 May 2026 20:15:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2825fc176a71c11e1e33764076755d76c746b8d67d1d93841d016a5479b8aa`  
		Last Modified: Fri, 15 May 2026 20:15:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d3d15a903abfdfb5bbd78b6b3636bd31cb2d3a98de631e3bd626aaf9424e1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c51491fde470acaea2d5a70fd83763373e227df5e3c59ff7e22ce907cd3747`

```dockerfile
```

-	Layers:
	-	`sha256:ea94b7abe31d2ced919ef1d664563ac78db4f4d6b029c1ea56904277da046f0d`  
		Last Modified: Fri, 15 May 2026 20:15:53 GMT  
		Size: 5.1 MB (5118644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45829319ff8e897e8072b2506a9b8d45e1a39eef65a36ee1fdd951db0731d5bf`  
		Last Modified: Fri, 15 May 2026 20:15:53 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:539ad8706c0f3444f2b982f288d993caafa510f6443f4149aa13afdd0b7818c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254300992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159e08cf1cbb6f26a9b401d1d12e7ee841d28abf79770604e710b05939ada5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:22 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993aebb06f4a6a2fc8a8c24d9bb14af299981b7f4d0cc8558565c16aeec61013`  
		Last Modified: Fri, 15 May 2026 20:16:01 GMT  
		Size: 156.5 MB (156461329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ddbeed0b44dcb7a476a4992a4d649488ef40c0b65a332d227d86a63c54c1ee`  
		Last Modified: Fri, 15 May 2026 20:15:59 GMT  
		Size: 69.7 MB (69722455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc8613e534ba510680eeffd620f855d903f8c65294cb49677af986f44869eda`  
		Last Modified: Fri, 15 May 2026 20:15:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e77f5286d170f8f14f4df85936601e7a2588432f807883a72e5a05ddd378f`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5490634d13be049e24deee73180db1abdbb5a59e8e827d1d23dff2ae86989c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2301ef67838f988178beeccd64fbc56173c377a208046d4cf1acac03be6234d`

```dockerfile
```

-	Layers:
	-	`sha256:824e5255749337af295dd663ecd9e8997ec5f31eb50e1dece1d4f3118f14a5d4`  
		Last Modified: Fri, 15 May 2026 20:15:56 GMT  
		Size: 5.1 MB (5124405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea55bfd0bb5d9638568304cecbecc23b1c00ac275df9dee6c4599ad62d28afb`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:271970a47af2222d50c90aef678a3ea9d0bfc34522f0e58bbf22c791f6487ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265988781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00f32881a45d4bdbd020d9d0cab62d2b16b7b2a92d22f16657022fd226c06b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:36:33 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:36:33 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:27:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:27:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:27:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:27:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:27:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7fc9485b4fb59cd58fcb71fcd4db3dba936648eb297bdcd72a79d669b2338`  
		Last Modified: Sat, 09 May 2026 02:37:42 GMT  
		Size: 158.3 MB (158343237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cd2adb362d11fcb1a5e086f0216518896c0f40e2ab8dad4184852febefe456`  
		Last Modified: Fri, 15 May 2026 20:28:32 GMT  
		Size: 75.6 MB (75566047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ff3944e4c3a67b9cb75c35e428baef88d7ea051db4c83e3f70f456de15118`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a83443dbf2bc863fa6949281046762768a9445e2ab8511fbe40056303c87a`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27841ee5d83e3330a40f3fa9de66a3cac7590a33593fbef3957ffb7c0ae32ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ef6a74ec0249b3cbcd6d092a662e56f9188f3845b25623963a0437bc35506f`

```dockerfile
```

-	Layers:
	-	`sha256:441a05a5d4f0a9bbeace70a107821df6723d3e65b56b4dae4abef6c02b8f65fa`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 5.1 MB (5123802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abafa2deaade04965746f905176966b875477bcfb3b7422056662d3e513ff04a`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c5820b219ec1825204826ee4490adcc7638e72c435a0233125ea1015f1a4fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242825358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae118ecec7c147430fba7d39bb4d324c94c13b2f47132b31754ef2e9b78f6c2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:43 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:35:43 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:27:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:27:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:27:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:27:04 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:27:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0809ac89c26156735efc3efef86a8d96aae2e4f1b2e41c915b45551d2d163af2`  
		Last Modified: Thu, 14 May 2026 23:36:24 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee44e1c9b9bfc8d1c4a69565a8a5f8665758efc6f844778c74ca3bee9238b7a`  
		Last Modified: Fri, 15 May 2026 20:28:25 GMT  
		Size: 68.5 MB (68544374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293991705030ef728d8fb0800ec9064545fea69badb17242f407d2013cb660ce`  
		Last Modified: Fri, 15 May 2026 20:28:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a49d98e0a24538bcb042586c06f8ded3242d39555e9d86ad92617748c43ef3`  
		Last Modified: Fri, 15 May 2026 20:28:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebf79f4bfa59377aebeecbb12d5e5ad7576bcfe4ebde73e612914e990bfb6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902fba0c3b3bccb26bf905d981839b8b2f4fd10e7bfd6102dff239c0e60a8baa`

```dockerfile
```

-	Layers:
	-	`sha256:1e3029fceadf6989cc146f9e0deb2992a9ee939ad1f11697dd53877304c4081b`  
		Last Modified: Fri, 15 May 2026 20:28:22 GMT  
		Size: 5.1 MB (5109965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a0621ea8ac3e634bd7f76c5e201bd8fa2ede464e66f9054f446d83641db764`  
		Last Modified: Fri, 15 May 2026 20:28:20 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
