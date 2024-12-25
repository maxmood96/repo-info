## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:9cd8aa79373ca9d5034071a20e1a872e0786fbff04ab927c34daca7d468319c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7ddc00287eb674e10416ad2b315546a0e4a3de09de48e7ce7d8eb9f0510f3c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280468510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8cbd451a6b250e9a406859524f8d8a23f0952ce039765139cbb98f020d6193`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7028d950048f0f0c8e712fe79f63f332ab6e074099dea621eab178fb2d13d528`  
		Last Modified: Tue, 24 Dec 2024 22:38:49 GMT  
		Size: 157.6 MB (157568721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1aaf5f5183c66718ff3b2d5b0ce64d521a4d8455e2d8dcb3f932368697aa2c`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 69.2 MB (69159792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3205c2cb22f64febc1ce476e56a1ceac037fa6dae0c19609d1cbdf06072c7f`  
		Last Modified: Tue, 24 Dec 2024 22:38:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c713be30dcf9371ca98f5360ae94d1a2eefc80e9fc82adaa4591eb031b9cecf`  
		Last Modified: Tue, 24 Dec 2024 22:38:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d1d153bef753e04953a9a28581df1ae0d0402ecbd5d90c7194a9c1b16c707837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c41ecf31d391b8d8d5cf1d9607c999d7a7eaa37866615640fee667d6df36d2`

```dockerfile
```

-	Layers:
	-	`sha256:4dcc8077facc8449984575a34fced7a083b9549707e622de11f6a1ad282b1df2`  
		Last Modified: Tue, 24 Dec 2024 22:38:45 GMT  
		Size: 7.2 MB (7208273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4adbb09c6bd61da1518bb6ba6b7f935ac94583e3af2a7311abfadf7053f6a76`  
		Last Modified: Tue, 24 Dec 2024 22:38:44 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61b1ca0aa5c8c6b9dc9af52b65576e51b1a860986e7d3d5edd26bee14a671e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277325921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5eaabcfd73e72c36f2b43b3fcbfd731323f4b70a92e26da75043400dcc114d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1241a00b2c08e47f7320bdf5abd5eb13c51b426197535af726d7c54e86c5acd`  
		Last Modified: Tue, 03 Dec 2024 15:26:01 GMT  
		Size: 155.8 MB (155793113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e45d69aabe334befe2186e0e4ed233b72904e6a1c925cf8e0f20a8696afe52f`  
		Last Modified: Tue, 03 Dec 2024 15:29:50 GMT  
		Size: 69.3 MB (69285775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7cbbf8a05679b7d49e23426757bb567c694f5f86bc409fee2a376f6dc6e05a`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd142aee7d5d5de73e96e0bbc3c06f52f4eef167840d78c1400b89e7a933e8a`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fe7a02f2ba1b1079d21bd0a9cafe487eaf3ad0ce5e446aa5948f94c6bfc77bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7239616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390d4069e5e19279cc525859dfaf45eae97f0148465cef118f061ca30cd515f7`

```dockerfile
```

-	Layers:
	-	`sha256:e75a5c7467b52c10b5060609d6aa17436ababcc4a7fcd7f815f53c3be84892f1`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 7.2 MB (7222977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55638b02da19285f7ccd4655d9442afb357851b3ea36975db6aaf14bcfe93c93`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
