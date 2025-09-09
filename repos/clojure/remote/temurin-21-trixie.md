## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:3870f1b386c5fc350fa1997abc5c5c2061664c9c8fdc96a433ec28573d750fae
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
$ docker pull clojure@sha256:50b9494f712ca1d4b271c8e45a0ae23301b11494fa5e293f829693bc71e46230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292618966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0d90e1561d630e9bfd7720fbdf8043b4faa9dfd25b97c138f59b7a0d42ff45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7447535acfad3d98374e42ae2429ba2a857066ffe931dac2fd74770defbac7c`  
		Last Modified: Tue, 09 Sep 2025 06:58:51 GMT  
		Size: 157.8 MB (157804766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57f8eb5c39b8f74b594ca75e9b8fcaac2cad7fa141d6d451c35f572197ff61f`  
		Last Modified: Tue, 09 Sep 2025 06:41:26 GMT  
		Size: 85.5 MB (85533626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4deea573664f2e9258f6c9ef3563b4bd5e1a8bc98df3cce580a23b7ae29e0cd5`  
		Last Modified: Mon, 08 Sep 2025 23:08:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cb35d6a969997b98f40f7d226eff0e647259cfbe5f263c5593369e88118b91`  
		Last Modified: Mon, 08 Sep 2025 23:08:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6993cec8ac823f0d7ff9ee6fba66a5b0483658b575f18b1d8a8696329694aa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b8b95bd0a5112931d2a41050ed080460424dd068b1fb9500b585c8be1da009`

```dockerfile
```

-	Layers:
	-	`sha256:4b9585e4be4e42f2c314bf4cf5bf23be08e6e551ed9245c86f58391e6677b45e`  
		Last Modified: Tue, 09 Sep 2025 00:41:05 GMT  
		Size: 7.5 MB (7470615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343db5465424e1fd5ab0704dc1fbe7e3d8dbb1cefbe64f723245421854c024ce`  
		Last Modified: Tue, 09 Sep 2025 00:41:07 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f4ad622f825bad25f69dc237711ec16253f0c4a8649361ac8b4a811dd28dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291083885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d730ac5f30e885437cc77e62bc6e65bf0b5e317325a0ffa8bf5b612deba70c60`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b8ec4dfe57799747aabd4f4bb916cdbba1bfb4adac77585b07fa01524b4ce0`  
		Last Modified: Tue, 09 Sep 2025 00:41:14 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ccd34a419aa90c5bb5f70b9719430d5e3727c8055775b62eba0460b2bb6ff3`  
		Last Modified: Tue, 09 Sep 2025 06:41:20 GMT  
		Size: 85.4 MB (85357907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49377cd8453d99e281bd94bdf15c84e4552fd6fb07d2c647c3e9e36d42ebb3d3`  
		Last Modified: Tue, 09 Sep 2025 01:17:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff666f7669a338ec802c9a06838d87cf244337dce999ae1c38e8502b10c3ab2d`  
		Last Modified: Tue, 09 Sep 2025 01:17:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:082ae2f0dd4b9dc8dd2c73a90ea2b60e582ae63e94a5ec77fc6ac92c03fc30d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d554333f21534db18c2fb77d7c1c649d6a56c396883b48d1f6a988637444cb`

```dockerfile
```

-	Layers:
	-	`sha256:9c1396152d681b137db584a3dad4debd2e4b1f518701e99b7b0d9665e1eb8ff9`  
		Last Modified: Tue, 09 Sep 2025 03:40:50 GMT  
		Size: 7.5 MB (7477669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5178f5b3262ed5dfbc30e36cca81f652b23ff422efdaea9fd9a951ff3c30ef`  
		Last Modified: Tue, 09 Sep 2025 03:40:51 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d59d790460b9b6cd328d44a97e6258b38e6840ab42bd8f64b12979fc38ffd754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302010139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c05d83180dcfe890429ec740a03bd51218885ad078fbf3e2e7503cdeb0637bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4281549a30760c62bb7524db0f5fb7d783bb093efae10f5ef654aeecd3428f59`  
		Last Modified: Sat, 06 Sep 2025 18:50:28 GMT  
		Size: 158.0 MB (157963445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6747b3a329864692dd796bf348b7365bdf605400eababf81d822e8f78c257033`  
		Last Modified: Tue, 02 Sep 2025 09:08:13 GMT  
		Size: 90.9 MB (90942265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29357da64282bd6b03aaed048dad1f8b8aef9abeef7af505e3e5b6a6e3f12026`  
		Last Modified: Tue, 02 Sep 2025 10:00:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50b2f3e43858742940805fd0f47a6036071d15d6d003cff0f45a4eaf5aae8a`  
		Last Modified: Tue, 02 Sep 2025 10:00:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f8060dc1eabd62880c9faabe2f683e1352ef70684ee15da05f28f632853726b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a603af0b851f03e9cddddc6d707a00e18705dcb4134a3e12fa31ef53e057029`

```dockerfile
```

-	Layers:
	-	`sha256:f61e71f4a3c7ad14394607de0b3bdac11f87402cda07db46362f1c1e2429eff7`  
		Last Modified: Tue, 02 Sep 2025 12:36:20 GMT  
		Size: 7.5 MB (7470422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4793b0e34fd1b295d8fbc64326444c7e4e07edcd44ae34dde925198a4a11166d`  
		Last Modified: Tue, 02 Sep 2025 12:36:20 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f0ec434a41952845cefe15feadce4efc086c4d6686939c597bdeac57c292a132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285783931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8831a290f76ad2a03cb8c756b830c44452e3431fae81d79407f9b49ecb105a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0087dac0fffe14b857e4289752b127d35f6852d85ecaf918e04e9250b5e3513`  
		Last Modified: Fri, 05 Sep 2025 18:46:42 GMT  
		Size: 153.6 MB (153593446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abaa03974ca1d280d510cacb2ea2ed9d2f71a55620c3d8e8535d286c6b110ab`  
		Last Modified: Fri, 05 Sep 2025 19:08:11 GMT  
		Size: 84.4 MB (84425135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8bfb5f4c619767a596af4ec33d98184a361aee7f5a5bf01865d09ef9237807`  
		Last Modified: Fri, 05 Sep 2025 19:19:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca053a9e601688c327312428624b1ffde1b1468470e3ca25b37ae68dd39e4ce5`  
		Last Modified: Fri, 05 Sep 2025 19:19:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3f78124b2b203ee65056e45f9f35214ada2ca9d7042f26e5d545a316ce0af0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e6b07eaf533131c54804dfe221c24d049bca47dcd1639d4ec193ff1d5bdca8`

```dockerfile
```

-	Layers:
	-	`sha256:f5398da2012192184ea528ad4d86a32d5e3c8cfb8c048663013ab1eea9a01b45`  
		Last Modified: Fri, 05 Sep 2025 21:37:17 GMT  
		Size: 7.5 MB (7453916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fecd5b85deaca03a3bc576c2ab16f28e44ee5686227e164e6ca245581fcf678`  
		Last Modified: Fri, 05 Sep 2025 21:37:18 GMT  
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
