## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:5008fb2930e080c49939c74eb629b4b1ba034c9ba871f3d79aceafcba9e6c539
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1fdfd669272a5f8335df41cf9ed2b033f30b6974853da04ebb13d21c8a7338d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274011502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ab48439262c95373e68302397009e00c9642975757173ab6c271478b16f67d`
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a6cab36c20830b95d01b517152d301b25e0ecfa43087af5d2a3d00aa51cb91`  
		Last Modified: Wed, 29 Jan 2025 20:27:51 GMT  
		Size: 144.5 MB (144536692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc54c384f80de34f8057520e64cb26624460e9db4050d0c5e09e6a66f5ec0e8`  
		Last Modified: Wed, 29 Jan 2025 20:27:50 GMT  
		Size: 81.0 MB (80993808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2172bcf25d2d1af22bd4f263ce66e9b5a3fc3333427625d05aaf9f55c684841`  
		Last Modified: Wed, 29 Jan 2025 20:27:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12600d08987c601a815d854bbaf80d90275384d4007b1cfa971b993f34bddd15`  
		Last Modified: Wed, 29 Jan 2025 20:27:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a062dbd575b86f7ca39d141b34b0f93f2456ccb74d1204ba6e634ac6e3003f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79018312d6f0a4604804f2eab1f29992a936e13d9e7ce64ad065463b6f096733`

```dockerfile
```

-	Layers:
	-	`sha256:df6330b280fbd12c52b458460092de35bc2988d75aac581dac4a723f8235c6af`  
		Last Modified: Wed, 29 Jan 2025 20:27:48 GMT  
		Size: 7.2 MB (7171080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad98e2c7c7707cc66d25e95d016a41e3aee462735ea8afaca9e4b6a03249e6a`  
		Last Modified: Wed, 29 Jan 2025 20:27:48 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2a1b2bc59ac19b8d3d0684ba6bb1ee8e04085b1dd0b94a9f95c8a94833b01c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272514562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9158dab96006e79abb234603e92d23a17b55e5abbbdd104fe6f9f35b6038e4aa`
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73438330cfefba49a94eacd83bc99b6b4b7158496156825868cfe83a4ff8049e`  
		Last Modified: Thu, 23 Jan 2025 02:44:21 GMT  
		Size: 143.4 MB (143360985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855ad73654b11f73b2f3f6fc1a9acae07a4305b7a750b59de978f8c14e9989b8`  
		Last Modified: Wed, 29 Jan 2025 20:48:12 GMT  
		Size: 80.8 MB (80845643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8eff36a54c0bb903d6b3a7e170df41f56b85a50e1883fefab15aa3a232de8d`  
		Last Modified: Wed, 29 Jan 2025 20:48:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc478d912025fc32f87d82d2a174923d2d27df9245795d08df5823f5d7c6180`  
		Last Modified: Wed, 29 Jan 2025 20:48:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6a2eca6fb93dd3fc55d60cbb90656d80a25657d04c072aab31732462b6a798b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629ef92212857a14cf0de53af0b3f1e6cbb7e1193d0de87ab178f4399aa19698`

```dockerfile
```

-	Layers:
	-	`sha256:bd4be81ddd2980ee73fe1939635537a6b462a28402d5a5a3c7bd828b1198e491`  
		Last Modified: Wed, 29 Jan 2025 20:48:10 GMT  
		Size: 7.2 MB (7176843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283458b7f07597b44ebbf88cc09af4fe289278f03b805e501ee762a6440961d9`  
		Last Modified: Wed, 29 Jan 2025 20:48:10 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
