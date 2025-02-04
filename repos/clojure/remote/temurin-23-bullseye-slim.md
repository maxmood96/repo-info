## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:ab857d6f06f492e6e448b831d4d942f864d847fc05691ec099087093b1078571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:80c4957c84bb9ab1b3794e5979a3f35b6d8bf9e779bb51999f8400e702c6b0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254357631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075eacc04eff4955a4cc361ad3417b4d16af467c327dd5be2d1b7a0ae3884471`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e543bb59bf3484c371c49b02dacb0cc15502776cebd60b388b58afacc23ddf72`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b4668a66c2dfb80f3d6b7484d65ff76a287a93b3381a60beb892c4f2d3ad73`  
		Last Modified: Tue, 04 Feb 2025 05:21:33 GMT  
		Size: 58.8 MB (58787825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fff77cf2e66d3db2bf86c6dc50a6e0de0b27cd84b2f758563d4e8af5bb7a08`  
		Last Modified: Tue, 04 Feb 2025 05:21:32 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58aad227c7160e4e5f8bc3fc2533961c753b74d1ba1821f958ae23cc547fbdc`  
		Last Modified: Tue, 04 Feb 2025 05:21:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e00cfe58e44195f491e0e718744bd60b9028af0a0a5f9b481f5356a72a856ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdc3a9948078117278011af6bf26be195642ff93b97913e740518a141476c7c`

```dockerfile
```

-	Layers:
	-	`sha256:68263a494481b3313c0029de21454739555cf83a841d2a0126fdb624dd9f7419`  
		Last Modified: Tue, 04 Feb 2025 05:21:32 GMT  
		Size: 5.1 MB (5122072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa49af13fff0816b11868110306345463b85f62bcc0fe75b0654d01e8d1d949`  
		Last Modified: Tue, 04 Feb 2025 05:21:32 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ae2f4ed97c1479177315ad8011be967a2965f1feced8fe45132118056562a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250996327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a799e9fd6c7ab4e07dcce1fdd7ff820f2065aa4203756c503668c52cc9bcd2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb526c5d9257b008ce9e6f38b15ff60d85e230a9348d9b3dfd8794b4a0feb10`  
		Last Modified: Fri, 31 Jan 2025 05:31:53 GMT  
		Size: 163.3 MB (163341446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695d689ef1ed51c811a1d75f1c03bbb24dd3231f6c5b86e7d91bd5594cf9a92`  
		Last Modified: Fri, 31 Jan 2025 05:35:44 GMT  
		Size: 58.9 MB (58908926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb7d57d70f3629375489d375cb04ca5fb569e11272ef60e44f3a4ccee6c0e36`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008c0111ce523ea7095c41b55e66248605a76a180fe39b6e7a0dc68e3dd0739b`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74aa87bd8e8da96ca6efcd86a696417de9fd366b9fbee946911bbb056439a6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be38960fe9007ca4c621bdff6f7f5378bb20035eac1a5d3f773afaa4cadd8228`

```dockerfile
```

-	Layers:
	-	`sha256:4b9bacbeb743493f509e890b49d2b3fbafa5231f6f3df57f070fbc449d592677`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 5.1 MB (5127183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1ed2f8cb3d6e65fc1782169b6667e62572574f2fd28552024f206652c0f65e`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
