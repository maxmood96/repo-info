## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:58a465add64329afc82bbc3588610157e76abf927ce018f5a21e6235ae2ba59d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

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
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e543bb59bf3484c371c49b02dacb0cc15502776cebd60b388b58afacc23ddf72`  
		Last Modified: Fri, 07 Feb 2025 06:52:07 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b4668a66c2dfb80f3d6b7484d65ff76a287a93b3381a60beb892c4f2d3ad73`  
		Last Modified: Fri, 07 Feb 2025 06:52:02 GMT  
		Size: 58.8 MB (58787825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fff77cf2e66d3db2bf86c6dc50a6e0de0b27cd84b2f758563d4e8af5bb7a08`  
		Last Modified: Tue, 04 Feb 2025 05:21:32 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58aad227c7160e4e5f8bc3fc2533961c753b74d1ba1821f958ae23cc547fbdc`  
		Last Modified: Wed, 05 Feb 2025 17:52:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a56307c345510660d99c80411d03416b4e98355f4bcce27fdb263e4b5d11b3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250996477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d081145aaee7140f24c7c6ebfcb2098e18e9ccb655693575e97e4b9cb09bff9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99325087be61afbd535597066d8cb53ded2733e364a918534e5aba3076419709`  
		Last Modified: Fri, 07 Feb 2025 06:58:43 GMT  
		Size: 163.3 MB (163341440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3f26bfad7e90e08e61e6c77c57f8e806777f451b9f4af68effa72d7f75d4a`  
		Last Modified: Fri, 07 Feb 2025 06:58:39 GMT  
		Size: 58.9 MB (58909191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca88dda6bd1ff988e1a2f825bf874a51109539f0a321c59edc2b730a19e9b7a`  
		Last Modified: Fri, 07 Feb 2025 06:52:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8388836b69159c2e2d50a1807a3f20f2efd3f4a898b83de5b8bb4df39714f72a`  
		Last Modified: Fri, 07 Feb 2025 06:58:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:11d15f1b2e23b1be8356b0892c73206d3cabbc61cbe12c1c020bd927827972a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7188a50f41f1a048b53878d9b0def6ad1b67fcf6fe458d859ec87c1b274b6e2b`

```dockerfile
```

-	Layers:
	-	`sha256:c495d2e8b9de63dfdc85203961eea6956302dd0464b3016350aa5de072501e55`  
		Last Modified: Wed, 05 Feb 2025 00:06:41 GMT  
		Size: 5.1 MB (5127183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0cddc5d38b857c1989d460772d2b003d7a09199895ca1dbdf7c50b5a95a011`  
		Last Modified: Wed, 05 Feb 2025 00:06:40 GMT  
		Size: 16.0 KB (15995 bytes)  
		MIME: application/vnd.in-toto+json
