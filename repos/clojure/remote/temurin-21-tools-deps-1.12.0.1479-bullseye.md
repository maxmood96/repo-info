## `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:89717f2464c92881156e0e85c88284b8ea5df8dfba98b4f38b2280cf245b7db9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - linux; amd64

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
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c713be30dcf9371ca98f5360ae94d1a2eefc80e9fc82adaa4591eb031b9cecf`  
		Last Modified: Tue, 24 Dec 2024 22:38:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c59f6e342aa541fca6c59bec9aa69a7570bc16943670a6f4d8f900b41c7ccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277325533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c1cace3ccabb9f16ef85991055d27f6df146a2b4b625a980ca60da9fff937b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694535f4ad58a5e07a98ea1c2208c2a6006b008b6802972d46ab6cf2062885ad`  
		Last Modified: Wed, 25 Dec 2024 07:32:15 GMT  
		Size: 155.8 MB (155793090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5d5c5f70fb4de5af2d66040991ba429971b39a14dfc8cbc8498b94107c78be`  
		Last Modified: Wed, 25 Dec 2024 07:35:26 GMT  
		Size: 69.3 MB (69285706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd590d6f61aaac1bed669fd65a9ec38aafd31cc863b2b0c811c18fcc81f575f`  
		Last Modified: Wed, 25 Dec 2024 07:35:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc0372b028883276c6960c33fea60a00378b0c42e6919abb03b64e21e8eabe0`  
		Last Modified: Wed, 25 Dec 2024 07:35:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:43bf834e69c9c445b2ea6314d566e845b9bf139d02a9fde41cee78af4b27392c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f5afebc057ac02b802f64be1b65c12b969b19230f23b048dbf2c9d4479a19b`

```dockerfile
```

-	Layers:
	-	`sha256:f709183ef4b9e0833173822381cb995fe69e8722e8972bba328e0bffa81612fe`  
		Last Modified: Wed, 25 Dec 2024 07:35:25 GMT  
		Size: 7.2 MB (7213396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460e4e516fe727067e98cc99e298ce82f4bbad986c10b18a0a6b8ada536c05fe`  
		Last Modified: Wed, 25 Dec 2024 07:35:24 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
