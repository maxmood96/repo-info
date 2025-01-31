## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:07d785116a076d7f663a4037429002c8a2983aa72902a85ed3659def7755381c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8060486701ddd6786c8d595e497ccb537d85fbac79bd63c3b1eb1d55dcb95d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255330843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0004c0ef23ddaf54eb01e5e4910a76989068816f420d55f837cec81416b8ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bf46f80739e590b11027ecf30e83d62de382177f7d59b88add50236b2e4bb1`  
		Last Modified: Fri, 31 Jan 2025 02:18:11 GMT  
		Size: 157.6 MB (157585898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44df9fa64bbdb59495742262958e26802682835e4a36c32349cb3cd039b3d26c`  
		Last Modified: Fri, 31 Jan 2025 02:18:10 GMT  
		Size: 69.5 MB (69531487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc6d578d51fccf7116a53355e9abde8b762a7b91dae149375a4d3eaad134dc0`  
		Last Modified: Fri, 31 Jan 2025 02:18:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b65e246a96bfb77dc299b9ee8f5f9860357130c0a38fc65c39a9db63fa3e80`  
		Last Modified: Fri, 31 Jan 2025 02:18:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:effd0e09f1872728fdf9bde71be6cab977bfa1b3688fa34997bc4fd69daccb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0dcc52c9bdc90cb82ff2164f71ef2d7883e7497d253b8d4d427d5c896ab6094`

```dockerfile
```

-	Layers:
	-	`sha256:52a69f639d7f1b0b2b262ed851bac5ed31a1af1f839be999ec8430070dbcbba9`  
		Last Modified: Fri, 31 Jan 2025 02:18:08 GMT  
		Size: 4.9 MB (4916365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e891a4cfd9d57065bf53d8f144757959cb91790ed20372a66d42598e07fb133c`  
		Last Modified: Fri, 31 Jan 2025 02:18:08 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:398d32c1e3b046765b2a9999bb1cab6aa2053e2df44a7a9e3267986f0e62e90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253282961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0275db2a420a54aa011a7d53be4d7e59cd2169e5279ddc51133975b8a83df12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1941c697535fcd933d9c45096e4befd9c237b71ed44c19c94f024567caa09845`  
		Last Modified: Fri, 31 Jan 2025 05:20:04 GMT  
		Size: 155.9 MB (155859317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c9ee9e1b4d5687184aa6f9cfae92846bcdcd8eac3254bc96ca43b45de9188e`  
		Last Modified: Fri, 31 Jan 2025 05:24:58 GMT  
		Size: 69.4 MB (69381573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d6a752ba25d8d3ad8ffa1a78699595d08463a26115886e445b399abfdcd5e`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dcf026db8192a72d1f409b6174e738a67e99dfc033857b52475f380d681589`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d32e48a214622fa33f545cea3d066d8b1ed62307fe9678f18affffcdeba9eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc18ef9d46799f705a1d47ac2fe842a04a3ab41b7c12a0b49bdbd7f8ebc3b5d9`

```dockerfile
```

-	Layers:
	-	`sha256:d059c2101974007bcb29887d076294ba63552536185837a3f5d1bb4aacd32d18`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 4.9 MB (4922150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ebb7463e6bd4aa5940f9ce5cd612c01b578380b46206d4d2e3bda7d285ca4ef`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
