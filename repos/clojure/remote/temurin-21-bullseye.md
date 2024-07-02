## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:a3c6d0710653d56e9d39b7c43017e87a69e53e949fc905d0b991848ff022716a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6763787f0222eb48e1a67e2fa6b8e4b743f487e1f476276721645a9eb6a6d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282601181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6750d5d521d7e90da3f9cabd251cdd8a465bab6cd6ba86cacad824b8f0df3c76`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
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
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc106e568c5c0475ed144d5fb0042ade9d77ac18c52df8e2cc7857651caf4951`  
		Last Modified: Tue, 02 Jul 2024 07:07:25 GMT  
		Size: 158.5 MB (158497952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5b1cd72ed8a561b3bd60a72f5c6d5e9013b06a6cc3604a800bd99ea45256`  
		Last Modified: Tue, 02 Jul 2024 07:07:25 GMT  
		Size: 69.0 MB (69020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9935acc1d2cbcf2ba4935ba2a5e38a5d7ab55afd4cb346eeaffed229ee052eb3`  
		Last Modified: Tue, 02 Jul 2024 07:07:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476b73a23ee3cc1f3b4aaa8c8972e639449351b5236981d6c5ef8c5bae20cdd`  
		Last Modified: Tue, 02 Jul 2024 07:07:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:72799ae3c79c61ace432f44a65c2eaffc79210fae953583160a2a8d48d7002c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd61ab350bfd3e59a4c9e488c9ec578b2feaf5919795d20b1b1d0808014266d`

```dockerfile
```

-	Layers:
	-	`sha256:6bb96fa6996809a28e239d73df5b69f04ebb0d6e17303bcf770fd9d8c6f263db`  
		Last Modified: Tue, 02 Jul 2024 07:07:23 GMT  
		Size: 7.0 MB (7000476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa4e2307ddbf0dbf3f2bbca983bf3126d7bf93e65e8a997e3507d6d90136169`  
		Last Modified: Tue, 02 Jul 2024 07:07:22 GMT  
		Size: 16.1 KB (16115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:623cb578ff5fb1dcfabe616bb8e8b900b98cdb562f733ea7cc880700f83490b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279522234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f686001c5c00d0402761733a9db7ec44e4968eb97207ccd204bdd1a632ed8677`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
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
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecca8477e0397c040d15e67b7e57feb8812c304741394dbd74afe49b31a0365`  
		Last Modified: Tue, 02 Jul 2024 09:37:28 GMT  
		Size: 156.7 MB (156665627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d401c3fbd8be617206844e4b10a9a4e7dc3743ba28333b3b1509785466f7d`  
		Last Modified: Tue, 02 Jul 2024 09:41:11 GMT  
		Size: 69.1 MB (69133912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a166113cacf91ac9bff320a3790c92182730160eeade41964bf097f657bd957`  
		Last Modified: Tue, 02 Jul 2024 09:41:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aec5fe2c12a558a22bdead70eec566ecc360ae29a41226973c7c37600d84eb`  
		Last Modified: Tue, 02 Jul 2024 09:41:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2d517e4fb66f41ab57fffcbd83b9a4143ca6084e8852d2dd5f07741afbad10e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9612f04dbcc61507dbb2a8f2af63dd731af5d2d2720db56a4cfbdd838cd8197b`

```dockerfile
```

-	Layers:
	-	`sha256:c3abdef51398d53db546272290789b3670ffff1c7686ddc34b1dd925e94e0683`  
		Last Modified: Tue, 02 Jul 2024 09:41:10 GMT  
		Size: 7.0 MB (7006222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a107cebc70471620f7e0c871fcd65f27de0b19f6f171ae217a37ee98504defa9`  
		Last Modified: Tue, 02 Jul 2024 09:41:09 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json
