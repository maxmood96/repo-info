## `clojure:temurin-23-bullseye`

```console
$ docker pull clojure@sha256:4199ed83ba2aa4a0155c0cc5538f2944e75d15de45287e41449b79d954808601
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3851b77f0686e72c6e805bf67136469b5736ac9f9cd4a78d3cdc30247573904d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288247058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf26750d0c1a730a5c2aad4c7601dfbd254b8cd5680bbfe3342c0f5857b260c`
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
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5677422e15f022261e12225e1b7497c6f0c894f6a02923084d2b10421534842`  
		Last Modified: Tue, 04 Feb 2025 05:21:42 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5008d1f8584d08b12b67045e12bafb243c9e860e115d8b294aeb068507a481e8`  
		Last Modified: Tue, 04 Feb 2025 05:21:40 GMT  
		Size: 69.2 MB (69190964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e05b5caeb2311b6df6ece7e6c00b2a09a177e3aa2b13997785d178932fb9`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641d7ea35f9e818684ff8a27e35313b664615de5b7b364ba6ba86147438a0bd`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f9bd5cd5eeecc555a6b9bebf13eec9708f299c458c88a6ea974e45518123216d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4148b221341290c889704dfce9bebf04fa68ec3af2db60ae497a5c6d4b612afc`

```dockerfile
```

-	Layers:
	-	`sha256:adb31484f6e7fd0d1159784b67c14f45b9ecca12ca4eda4637beb4bafe5d4f18`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 7.2 MB (7209560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638cb5c5b39aa09e6ed44accefcc9bc855a8fd9780aeec25fe0232e6c18e3862`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5081e3ae58c3f1af82dfc6825087c5628cf1c4edc3a10844cb02c94ee9e99230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284900099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc05cbfe8e1ee39ab2bc7584e80da4a21f39aee7ce4bdfb20367e1f30c4b3a17`
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
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d25902b1a156d2737be48e800027a3516ee7b117f58dd8ffa32ef8b395161f`  
		Last Modified: Fri, 31 Jan 2025 05:30:51 GMT  
		Size: 163.3 MB (163341429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37fb0273db6bbbc1bc0d01939c2671a53aaaa39afd03368cc16ab8bca8be960`  
		Last Modified: Fri, 31 Jan 2025 05:35:05 GMT  
		Size: 69.3 MB (69311568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcb57ca20163bf99434becd6c24dcdd4c537d101ce523f6e2e974fd8dd682ef`  
		Last Modified: Fri, 31 Jan 2025 05:35:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e74640e33226527076db7ef67dcdc35486d9643d72ecc360151a98100c654`  
		Last Modified: Fri, 31 Jan 2025 05:35:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6b23ece8011ad4f83617969f40fdad31a276a10b6069924fd3d0c472caee5133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f866d2109b76f4d62164454eb8066e474255e319a0dff00d6c8de9bb77328035`

```dockerfile
```

-	Layers:
	-	`sha256:fe23f581e60a6ecf03cac6d25ec604b24a4d881997058579ba27168960ec2122`  
		Last Modified: Fri, 31 Jan 2025 05:35:03 GMT  
		Size: 7.2 MB (7214038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d2f4ee034d3fc20aa8bf291bc24f371155f2fe62884445500fe2cad225af549`  
		Last Modified: Fri, 31 Jan 2025 05:35:03 GMT  
		Size: 15.9 KB (15937 bytes)  
		MIME: application/vnd.in-toto+json
