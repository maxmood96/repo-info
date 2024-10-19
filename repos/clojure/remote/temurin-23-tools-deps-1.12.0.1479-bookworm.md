## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:d7d69b649e3e51d0b04e7c194f8967068acc064cccd429d25c64a6d4e6fa22e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f2e79b1fe2dd5d63aa09ff0963ef6182df05db2f5e98418a43808c4b1377e47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295751697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f68a2d16b4c91016f4f9e07315498d2e3781f789f309adcb7d1e407ed7ca9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0adeb6a7fc885d3cda46a56ac22253a40d213924efa704625e1b9d7f47298e72`  
		Last Modified: Sat, 19 Oct 2024 03:00:27 GMT  
		Size: 165.3 MB (165267577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971f616bdcffc35db7d37e224638a356dc9791b8ad77d542622da57c1cb102b`  
		Last Modified: Sat, 19 Oct 2024 03:00:26 GMT  
		Size: 80.9 MB (80928057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a66c22d2332c5b7d0fa892e736afb6ca802343e12f9a1740d270a004c37def`  
		Last Modified: Sat, 19 Oct 2024 03:00:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bc1be6392b3d44103519286c0ecfa382a4a73be45ea7e8b05931ec757c6350`  
		Last Modified: Sat, 19 Oct 2024 03:00:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bcf02e2b80959dda07fdf5a7340209279ad101d6b15e7867a149144bd41fb33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1fd0690224c924bab887d9217e0c354207a56b02200b04588f40457b9aca8c`

```dockerfile
```

-	Layers:
	-	`sha256:565392c48cdfa87fc199b3a0b412c23f8b771a1a9aa09656a313a98a3e09ae02`  
		Last Modified: Sat, 19 Oct 2024 03:00:24 GMT  
		Size: 7.2 MB (7188068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d2643872b8db4cb63acbc3e9348ead5198bb95875f3023597aa1cb300e5283`  
		Last Modified: Sat, 19 Oct 2024 03:00:23 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b50047c6c13d48a973deaa542b97482c788b395e86de2c87d72370fe142f1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293628876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1443e4667ab45c0fff19e759ced679093a3e875813928dff0a8b45eed71920`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72374e05c5fc01256ab2bbc23ee7744b5db54d404aac7042df98fa6ce9ce8f3`  
		Last Modified: Thu, 17 Oct 2024 08:27:41 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c02996c20eec70b7b6be0d70ffc26515007dc650ac86b317c732113f4f286d0`  
		Last Modified: Thu, 17 Oct 2024 08:32:36 GMT  
		Size: 80.8 MB (80790058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0573c624f92dd9292787ac2ba42af96d4ccfa47246e5145fa0d49b9bf81507e1`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c38732d38f1ffa6cf16dbc734e4d766fb150c311429f25afc12dd4d3ad342b7`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc0e61afa2ee7fccd2aac0b2a03c53b1d8a3dc9fdbcd3c3ca2dbd610f303188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3cbe4fc8f4a7e3b50e850ce727fb0bf4cdd300d36c5ba3c4ca2b6e70a5a910`

```dockerfile
```

-	Layers:
	-	`sha256:defd3a071e6bf83d1e6709315ca6ff0c442c223944e3bdc831a1f43b614b953d`  
		Last Modified: Sat, 19 Oct 2024 12:22:08 GMT  
		Size: 7.2 MB (7193238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4192d95ba817ff69d1d2312af27c097199963e291f4fce37e1b1cdad29775b`  
		Last Modified: Sat, 19 Oct 2024 12:22:07 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
