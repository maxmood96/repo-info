## `clojure:temurin-25-tools-deps-1.12.4.1607-trixie-slim`

```console
$ docker pull clojure@sha256:4d0dbeb1602ff6f2e46b43876920fd8819e2d32b4259f56a35da16853de96b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1607-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3981b8344266315c575442bc70068477a343346e67ba569ca0147cff8f162e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194044471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53afc79a3331cb5ff50a3d99cb2ce094af8445df671591067739eb44eb8e1dc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:39 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:39 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa5e67ee2c3682567cb75f954105a0915baf0672e3dffbd67fe0405b814ce97`  
		Last Modified: Mon, 02 Mar 2026 19:49:13 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3232227cc9f683c5033c235d06098cce14de4ece8ab7c41785d01beedeca2eb4`  
		Last Modified: Mon, 02 Mar 2026 19:49:13 GMT  
		Size: 72.0 MB (72008498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68ef3923237c9b24e04db5e8a4d5e3822540a1661dabcc9261e57797a107f9e`  
		Last Modified: Mon, 02 Mar 2026 19:49:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b296f428b758cef87bbc6bc36ba9c0576b9f51578fd09549ca184cfc7011de9`  
		Last Modified: Mon, 02 Mar 2026 19:49:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2121aba58def592134487af048233ccf0f5eb0f7f2747d48250a01297723cb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8198cd94b5431f308a4b4949fbf0b9a8de3bd7a1495cfebbd31540d6933ebe5a`

```dockerfile
```

-	Layers:
	-	`sha256:9213c63012fb4520c91a8ffe5b69c46ceb1268f0cc45201ce00ce65693587ed9`  
		Last Modified: Mon, 02 Mar 2026 19:49:10 GMT  
		Size: 5.2 MB (5227150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd04f48abfcf6b7ed9639fc7c17ed60c9d2f823972350c58b7900710ca97fcf8`  
		Last Modified: Mon, 02 Mar 2026 19:49:09 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1607-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3b0fbf0e095817730788f4d7db6c6524943a10198fc380a7fa1827fd7554d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193253480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36db129651a2ccfc37cd513a5a20b04f6296bebf07da895b8c9c7f6b47e2e788`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:38 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:38 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:57 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dbf3642bd4b9af9eebc50813eeb5913d6205414fc86b1a98d9496a5934e0fc`  
		Last Modified: Mon, 02 Mar 2026 19:49:19 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772900341c365d62ae175929c1fe5c3bf2de1fba759bc7a13b76ced371791a1c`  
		Last Modified: Mon, 02 Mar 2026 19:49:18 GMT  
		Size: 71.8 MB (71824065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6c291b9fce91535730bed2f26613bb98419cb17edc090eea3bd7f983da27af`  
		Last Modified: Mon, 02 Mar 2026 19:49:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ae5545989ad8edeb9a6087220e4ac63b801aefe060342cba5636f8483faf2`  
		Last Modified: Mon, 02 Mar 2026 19:49:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18a0fc074b2aa9ce7f71a7dbeabd49e237756131f36ab001e9641226531821cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2d870fac65da5412ec97d4d612aa36c8adbabf711371064bd0e905d608db39`

```dockerfile
```

-	Layers:
	-	`sha256:6cb32c13293efe7143cdf259a0a2d0ae19b8198af2bf5fbcaa2f62e70d7e8fa0`  
		Last Modified: Mon, 02 Mar 2026 19:49:15 GMT  
		Size: 5.2 MB (5232940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab5c868b0972c5247fde965d1a3102143eaf7f15af44a20e757a03fb69a725ff`  
		Last Modified: Mon, 02 Mar 2026 19:49:15 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1607-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:174b706768d453c9ceb8b1e396813e178978ab719dde3228adb1efb836f546db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191045110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281eae90641d5920e927b487236171afd9130c48b554518abdca449905248863`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:49:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:49:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:49:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:49:27 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:49:27 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:49:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:49:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:49:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:49:44 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:49:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44006f62427397d868b9e3272fc3067dde899f0459c5a6ba908fc4bb1c1da8ae`  
		Last Modified: Mon, 02 Mar 2026 19:50:11 GMT  
		Size: 88.2 MB (88233834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ffe9cde78de489adc9fcd20e7dcf7355621a105b09e680aeb2340ae7d35b9f`  
		Last Modified: Mon, 02 Mar 2026 19:50:11 GMT  
		Size: 73.0 MB (72972055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107fc08abd1279ac5bb88a65b4af2dad21f20043ad96d7bcba066411c09f14dd`  
		Last Modified: Mon, 02 Mar 2026 19:50:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13053a04edd39ffa44f1bb6ca4a1be980a3b0dc7cd7de0179e21a9e33f8e0657`  
		Last Modified: Mon, 02 Mar 2026 19:50:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:404fc1365ea475fe07092ce2d3748bf815ad70086584ec6cec6d4a874ab389fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa4694ad0ce937d25b40a7c809be8333214db255862a17731222bacae38af4e`

```dockerfile
```

-	Layers:
	-	`sha256:b5f3b2a26409222f00abc935599b879a5593d1fe065bbc7bc8505be8a4da9d5c`  
		Last Modified: Mon, 02 Mar 2026 19:50:09 GMT  
		Size: 5.2 MB (5207636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077c323419d2a2214fa7850ee5f52cfd7bc5680305cbaa0435254e86e225218d`  
		Last Modified: Mon, 02 Mar 2026 19:50:09 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
