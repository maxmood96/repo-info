## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7196057b3e992ec9a1442cd1bd209d54cdb6fc9748efc30b87af49d7040fbb92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0383d2cf3394bc9e4a2b23aadfc85f4c352817b6a8944d5528bf8e01158c6150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215352865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ee844b6a267d6ac1365d91bcce90626b23aad868157afe08534abbf3f60152`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910342737b2a9c7cd5f19aefe067e9995987b73b263ccf5a3927a756af42ea95`  
		Last Modified: Tue, 30 Sep 2025 00:57:12 GMT  
		Size: 92.0 MB (92036051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0f639583bbad9db683d451a2a3bb104775ec2e9f40d0693456f64d2fe9cb0`  
		Last Modified: Tue, 30 Sep 2025 00:57:12 GMT  
		Size: 69.6 MB (69559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72dcfa482d985725aa28a59ffb8170e464e9c87dbc34b6c61d67c4846617272`  
		Last Modified: Tue, 30 Sep 2025 00:57:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036666dff72f40c1ea01b185fe11d1098eae0fd76f14c77bfa582d05a185a120`  
		Last Modified: Tue, 30 Sep 2025 00:57:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dadf242f437e5c477c9fe250cdda8443090a6beb3d4026a6705e84ff847034f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200826a9869bc84530f74345895afa6dcd185729e4ca0c174e8d50e5e45f66fa`

```dockerfile
```

-	Layers:
	-	`sha256:6252b679764d7dec3371458be066bdaec0bc471db690ff73596233e92e0bfcb5`  
		Last Modified: Wed, 01 Oct 2025 15:41:35 GMT  
		Size: 7.3 MB (7346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:558d20174a7bce0c50d52b21cf8d778daf071e5b73c05e6727ba1d41e8b9f22c`  
		Last Modified: Wed, 01 Oct 2025 15:41:36 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21a3512799a1748d05b326424bf24720a492983c600d6f517ae3e675b36be862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212983149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f559a857a2c5bd7163ce5c1af8c9c08f494c7978433808d6b5be9e3140b808b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c79da623ebb8ed23fa67b62312631ae068565467408340d717026bc7b6009cd`  
		Last Modified: Fri, 26 Sep 2025 17:57:12 GMT  
		Size: 91.0 MB (91045230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbe0f9449b2734fe2bc4fff6a2a5c3c9aba82aca458b3d1fdac95de7a64f785`  
		Last Modified: Fri, 26 Sep 2025 17:57:08 GMT  
		Size: 69.7 MB (69688504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6eddad311182cf3d755d42a479575f6381c47aeda4b50db4d2888fb53d4842a`  
		Last Modified: Fri, 26 Sep 2025 17:56:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8821f2b090b68e3fd809cd98d2b18951f89e6a83259b7091753a6876741fa891`  
		Last Modified: Fri, 26 Sep 2025 17:56:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f0a7f19889e9f6370e412e54b4da72b22211092e7b9fb769124cc53876fa97d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cbf86905c58993fd8431807d32113d0900bccf1a8e681e65a4cf1d3b28e74e`

```dockerfile
```

-	Layers:
	-	`sha256:ec353e2f437674373ffd4432ab3dbc46ab4a965174cf4e3900c12d65170017d9`  
		Last Modified: Fri, 26 Sep 2025 18:44:06 GMT  
		Size: 7.4 MB (7352113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1def3cbf7d062037d33d5dceccfc34a946f464d7bdaf6d64d688b33ad2f6cc58`  
		Last Modified: Fri, 26 Sep 2025 18:44:07 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json
