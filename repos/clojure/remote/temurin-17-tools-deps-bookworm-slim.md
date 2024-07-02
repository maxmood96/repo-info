## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:55335e593131e25a6e7bc4b3cf81c62e1686afbc35884bc7821473eff5096d88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:60282659b40960497013ee69091c8fab7458530f9681ed1e3e7bbc9dfd7c737a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243289074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c868ec19c502e7b0f76c5fa0d5f3232f216e0a5a2b7efda3d3acc546ee9b93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569016283d02dc8ce9e9fd364d8a761e1c14edea190e83691f0c2d70f729836`  
		Last Modified: Tue, 02 Jul 2024 03:02:55 GMT  
		Size: 145.1 MB (145095109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f143a6384781cafe2c92fd3ffcf2069561c5b6f5d1fbc4660b14dd093484370`  
		Last Modified: Tue, 02 Jul 2024 03:02:59 GMT  
		Size: 69.1 MB (69066645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835402ddefabed1ec3d86cafa6087dc716a4bb4b2e72479ccdc9ceb56e235054`  
		Last Modified: Tue, 02 Jul 2024 03:02:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9481859f3204860c9b886f7e1c686e8aedfd0e8dbf4360a22f7cb2b3ed1d1c2a`  
		Last Modified: Tue, 02 Jul 2024 03:02:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd8f44ab3f3ac5b57bcbc873ab5de8b6ff6643c3570efedfaefe6e076d594a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2199ed3a2a722e321101f48f08b0d12e0a26a65ae07266a8d505e2706c894627`

```dockerfile
```

-	Layers:
	-	`sha256:f120738d8a0c046119e9eff2d11fbff4b373253d25679a0260501cfbd3a8265b`  
		Last Modified: Tue, 02 Jul 2024 03:02:58 GMT  
		Size: 4.7 MB (4705039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900a193ad03555da83846163388371ca71b1401ca5b6a3c94ae9f517492da3c6`  
		Last Modified: Tue, 02 Jul 2024 03:02:57 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:579c501f2308815c6bb253d326e22571c554424e9e530b29dd6d43ed97edbcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241694374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b1850a97a4e93c62d5d76ef9c6de818afafbd21b632a3a243f0749732e753c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22608349e93829bba81d2d208b5bb14cbc7cb9450f4d75e80ac257e503978d5`  
		Last Modified: Thu, 13 Jun 2024 11:36:10 GMT  
		Size: 143.9 MB (143892766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbd9b37888c8808647b02d46fa609aa6e90204490f99c48b3fa1397754bc207`  
		Last Modified: Thu, 13 Jun 2024 11:39:30 GMT  
		Size: 68.6 MB (68620895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95033a0ee28816eceb2eea35b89be11505b0eef35f924f05f9cc3087753ac991`  
		Last Modified: Thu, 13 Jun 2024 11:39:28 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d723d18fcda060a87617371d4c00756a8f5e4d7f66156b9edaf5afcda9eafaaf`  
		Last Modified: Thu, 13 Jun 2024 11:39:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:61a9d77000c99c110f6019040169e3284a88e28457be806be005a8e3560bdd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07c1ce7eb3d68240f822c315bbd72756dfb23fbe7488e00acc12dee7dad2ae6`

```dockerfile
```

-	Layers:
	-	`sha256:628c8adacffb3f4826bb5416ed54b328e2533e6cc94303a75c4403739b28511b`  
		Last Modified: Thu, 13 Jun 2024 11:39:29 GMT  
		Size: 4.7 MB (4711323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849a35f6ee6602e4ab8a5838196ae3bf29bd725ab8150bc2cd5def4170fceb5b`  
		Last Modified: Thu, 13 Jun 2024 11:39:28 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
