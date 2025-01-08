## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:0e6e7c2ea6c201a79c92d317c84d456fe55d3ce023d6e4d000e4a044865e9f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c294e38bfe27ebfb0c6bbd38c5a8f2aaff85c295e6aa035ae87cc0caa99af08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243146230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15495ceaaca9ebaaa30d16d9ff09bc0238532d32e34c0c7344e744cd8af2f20a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7acf14348431cef92337a1e8784946fa889d6e2abeca9accf69583f78b541c`  
		Last Modified: Tue, 07 Jan 2025 02:29:22 GMT  
		Size: 145.6 MB (145601500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2969d0a9800e48fb2e6a5200e4a006fb4b59e0e08827b95488373766192db981`  
		Last Modified: Tue, 07 Jan 2025 02:29:21 GMT  
		Size: 69.3 MB (69312508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01baf049ce081b6db4b24e2995bf25b2bd5371ce26ba38fb8bab5b457450871e`  
		Last Modified: Tue, 07 Jan 2025 02:29:20 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:339b40401381ebb62b72ebe2dc84ee2fa4a11f9337f04deeb0ad119772202793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a724e2d57b9b778d7d7ab03f796728b1d7e2a98b5fe3d6d679b2c3ffbb77d25`

```dockerfile
```

-	Layers:
	-	`sha256:cf7cad7d8b6bbffe0e81a05939b88100b12e7fb2a355c033005e3541eab8303c`  
		Last Modified: Wed, 08 Jan 2025 07:29:05 GMT  
		Size: 4.9 MB (4932708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca23592d73d5c91b508aa36188abb4e94d60c9849c190cdedd4bbbc337ba91b2`  
		Last Modified: Tue, 07 Jan 2025 02:29:20 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d35135a9fddb558b57bab3858b399bbc3e6178c111a61d3cc6d40ae5de002bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239618636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d443269eaea687363cf93fdb7beb512e1fe19eb47820df7bbe88cf6dd984cc3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb81eefa71bd631b66935bc0c6a842daa9ef69a8d87d3547942afd439994d11`  
		Last Modified: Wed, 25 Dec 2024 07:19:01 GMT  
		Size: 142.4 MB (142388995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dece501cd802760c6659eb3a79c5e6ca8dff1406e9c6170a0c18fb9eb32af6`  
		Size: 69.2 MB (69170273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42390c9b0c40303a421ba0c053114fd5c7f2577a4340471ca69999d5fbaae044`  
		Last Modified: Tue, 07 Jan 2025 03:23:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17851a59f5feb404ac576269b6b574c2e835e06f160ab263b37b774c80342c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc255e2b86acc59f3bed22a0c8a75bda0891263bac382ea17de4a9bd4c3ad006`

```dockerfile
```

-	Layers:
	-	`sha256:a8b201d1d14c9bfd771c5cf0c2a8dcb5c3481f08be1f238244f892a30ee7b97a`  
		Last Modified: Wed, 08 Jan 2025 07:29:08 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961bc8d3cf78eb68ec39d3cc1ac68a57b4802af6f2ea9ca64a15899178e8558d`  
		Last Modified: Tue, 07 Jan 2025 03:23:04 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
