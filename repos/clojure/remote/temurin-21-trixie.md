## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:3aa311a057c253d3b0c52fe976ed65fd9eea2da0eb2be27032853cbff40e1c86
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:972a89d7673000de20c9776181b1b3f4a5e8843e5b283e2379944678c5955c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292619225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9239b7d9b86545d9b81ae8f4e2267d1e52095aa02be0bd3a84d72467170a801`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d66287ef4e4f7a67ee2c73fadae2b76dd2df655c4c6767f21cdf59be876c578`  
		Last Modified: Tue, 16 Sep 2025 02:01:52 GMT  
		Size: 157.8 MB (157804768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356caebdfe8428f6095529608a8a8fafdb6ef9722aebb53bec1569b2648b8ec`  
		Last Modified: Tue, 16 Sep 2025 00:23:46 GMT  
		Size: 85.5 MB (85533882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6060dc193bc398205824dc362e51b38b9621e1a17bc2aa29b2a7972975cb8a0c`  
		Last Modified: Tue, 16 Sep 2025 00:23:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0546440b454df3dba5ddd70663cec9b4feea23303775b3ce1cd3d8d26c779417`  
		Last Modified: Tue, 16 Sep 2025 00:23:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e493a86c94c65dacbb7b4097b29ff8d7887f10335ea72e182b641971ebf19879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e8424a77c2409219ebbcc5a91857189016b05d3a6ececf483cbbaa4698d487`

```dockerfile
```

-	Layers:
	-	`sha256:cd8e6ea699a08d4cc5a2ef7f9b2d4c42e963383b835409193e6dfc20e08b7c27`  
		Last Modified: Tue, 16 Sep 2025 00:43:42 GMT  
		Size: 7.5 MB (7470615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:affd59830ec7d478453153087f214d639c17c470b7a4d8d3b9693914decc8dde`  
		Last Modified: Tue, 16 Sep 2025 00:43:44 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bde9d44c6d99c7409498fc4d513c3d6923668295b64b26cba4873c53969be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291083301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fda492c148a7b2ff91990348b86bf12f64d59c7cd7013cc6b461d72c23bfcac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536e0b6030c31eba8b2ad6c1c51c09cb40eea9327ba38b89b73517856b3bc0df`  
		Last Modified: Mon, 15 Sep 2025 23:28:09 GMT  
		Size: 156.1 MB (156081218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec10b4f3fe122bc7d089125145ffd44f8c503bc0d8c6e9da6b2c76893dbec954`  
		Last Modified: Mon, 15 Sep 2025 23:28:08 GMT  
		Size: 85.4 MB (85357296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fca724d319940c8e032b38bd79a50f31c70fe80b0ffb1e71c6c8dcd7bcdd12`  
		Last Modified: Tue, 16 Sep 2025 00:12:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562c50aef406de6288f7cb67eeee42511b7f4da5403125490e1cc867f3be3a2`  
		Last Modified: Tue, 16 Sep 2025 00:12:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b18cec9da18fe6fcb8688308670eab62a0ec0da7c1c2c03b2afd0e63a8066343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ddd8627adfd08460d54745990f1f79a95795c2fd04a85d61611ef569c9994f`

```dockerfile
```

-	Layers:
	-	`sha256:60837c32b0932fbaebce05ae72f2f37a894b13a7ddb339bb3011bc67b11553ed`  
		Last Modified: Tue, 16 Sep 2025 00:43:50 GMT  
		Size: 7.5 MB (7477669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703b966602266da5abcdfa8c6e394c78b29bdfcebad793fa5db608ffa311574a`  
		Last Modified: Tue, 16 Sep 2025 00:43:51 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9cf4049b2a31d0afdf98aa7c9a845215f18eb99b8647bf398c7ada21d5660d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302019623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c3579770e73bf1427c3a43392f97dc754cd492c1c3d9aaf4eef41fc0932967`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8817d574c25256f5629b3a48d1c2f281840eca84d9fe69690642c6a7ff7dfbf2`  
		Last Modified: Tue, 09 Sep 2025 12:36:51 GMT  
		Size: 158.0 MB (157963443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c595ddb1a34b64355494c0b616e84edcbae0a88788efd650392fbdc3824f539`  
		Last Modified: Tue, 09 Sep 2025 12:50:36 GMT  
		Size: 91.0 MB (90950704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa420d4122c3af9440526fc478b5f22601fa09d22a0c4a263adea6348f8676`  
		Last Modified: Tue, 09 Sep 2025 12:50:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3360ffddea59fb6de5cf285e235a3af26953072f78c4e4410cf81cd52f7d4e`  
		Last Modified: Tue, 09 Sep 2025 12:50:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9dcbe19e50c9d7a071d7b9289a07609d1d92dd6753869b4bcaae769b45ab402c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782dc7382e84c6faad1689327dec5eaabd5427990c91e3de4b5e190117610dd7`

```dockerfile
```

-	Layers:
	-	`sha256:483db70f709cd809c295dc4f653687c436e9a3909977964c875614c00587663e`  
		Last Modified: Tue, 09 Sep 2025 15:38:51 GMT  
		Size: 7.5 MB (7475046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24f288d755de237fcddcf9a9aecad27e7eb57017638944ebd54ebf3046e1de4`  
		Last Modified: Tue, 09 Sep 2025 15:38:53 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:ff65d426d93c01020de91098440ec1c097146f32d639d6b49393cb989486f747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285787387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff88d1981255241998e2eb2b4323e0b5b509c62fb4d8228920ef43f46486ce2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d16d1a64bf63ce2a46fd192fcc03ef4725134c5c609d93baa2aa37b68e7d97`  
		Last Modified: Sun, 14 Sep 2025 03:36:09 GMT  
		Size: 153.6 MB (153593506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed86bb11901dea3cffd31c97117d962c8d9a19a36be391785bedd8cf40cba5`  
		Last Modified: Sun, 14 Sep 2025 00:13:48 GMT  
		Size: 84.4 MB (84427388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a26ef8d9cce39df7eadd8b36f99c4f0a2c3465ef80d74e0fd44b6005ee2f2`  
		Last Modified: Sun, 14 Sep 2025 00:13:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a66af2f7b793424056e43ce2eacb2b2d886f62714793c60560e7e349f287c7`  
		Last Modified: Sun, 14 Sep 2025 00:13:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6fc4da5458c93480be8bb2c54130354a7b1991289e52016c3335836c4bb426f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7475065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbecb325ca202cec14e3adb3155288398a2dc6b98f901129e4855336259abae3`

```dockerfile
```

-	Layers:
	-	`sha256:0fb084caa48a91601d76a02030b661c2005799ccdccf3e1193821df76be6f5ab`  
		Last Modified: Sun, 14 Sep 2025 03:36:09 GMT  
		Size: 7.5 MB (7458540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f493253879485a335ba0c87cdbab46a3c5b559a765aa3c2c24b0f2c209eabb`  
		Last Modified: Sun, 14 Sep 2025 03:36:10 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:379dfcdc236cdb3d61e1426627dec20b57e9384bea469fa14a9b5bd750466701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282880266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6bbf15d088b8a685230a504bf62b9a3d92eda36d8df051b9e119dcb195adfd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50c8c2e93fa05ff72af8f6efa23a3b9417e7eacda877a3cd9b6e210f76182de`  
		Last Modified: Tue, 09 Sep 2025 05:49:38 GMT  
		Size: 147.0 MB (147027052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fd1335c5d0c916c3b914a8b434591f548bb8206c4da26bdbfc2b682b2c3bb`  
		Last Modified: Tue, 09 Sep 2025 06:41:23 GMT  
		Size: 86.5 MB (86505849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a49aa13c340ed535eeeaddb7cf71ade28062a4342c2b2d878c329fdae1043c`  
		Last Modified: Tue, 09 Sep 2025 06:31:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c904c9cff57e08e6ba81c1ce1092e8307409ec12e778bf15fa51feb6244cde9`  
		Last Modified: Tue, 09 Sep 2025 06:31:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0dd2086c3a0e6062179890ffabe70728a45f2f8e13b1065bc78f51582579128d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa729550961afb58124e48ffdde99bbe0b25e74baec74fe330f31e51ea71cea4`

```dockerfile
```

-	Layers:
	-	`sha256:e736f085e5cac4fde56484956f1460bdfb46da243499d908a345433dc47834c3`  
		Last Modified: Tue, 09 Sep 2025 06:39:26 GMT  
		Size: 7.5 MB (7466537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0996370fd3b22d85f4eb967c070ec51cb5e85fb59e0028f053a086d4c33120e8`  
		Last Modified: Tue, 09 Sep 2025 06:39:27 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
