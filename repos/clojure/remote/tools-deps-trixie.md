## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:7fbd9285a6c9a1c8df2d62d48c0916c8f1136ca03f866454b1d8d28e4311d414
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ea9621b7e1903bb7390662a46aba7e24e49af38b5e33b6e44e1a83e9d47f397f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295089776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bbb4fb95bfc57b12712fa484bfb9cc5fd97f092df8ea7d6023d988b73d31d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03af077612f84a578bdbdb482d2afb41dccce23b628e7d5da92d969b9e38eda5`  
		Last Modified: Wed, 04 Jun 2025 05:45:42 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ba269871c7322da70623db1f93557b931f3e77c4d7a2f69fd8a2d578269e87`  
		Last Modified: Tue, 03 Jun 2025 18:24:49 GMT  
		Size: 88.2 MB (88207326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c951c45fd6fe404c03cb7eb0cee956505e20ddc6aa55b7caa99af2a63a22d3b`  
		Last Modified: Tue, 03 Jun 2025 18:24:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500de711a2f28e79566436a44d510384ee262c802484715e3e3817223c3db329`  
		Last Modified: Tue, 03 Jun 2025 18:24:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b07e6c2f540c0bc15e770d603d167ce8c8945efb37315dd07b79f250bdff92c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d587b1ba6d83efec0cc4265393a89a8d8c81e8b8208c872d572598df34b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:ad40b138560168bb8956c4a28cac0c4e5b187ec22cda11bdf1ae6ce128922b79`  
		Last Modified: Tue, 03 Jun 2025 21:41:23 GMT  
		Size: 7.3 MB (7322186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85e5690f180c26eec1efe46ce6869abc0d87aae2a16e8ed9e36390494f0548e`  
		Last Modified: Tue, 03 Jun 2025 21:41:24 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e11d59b846f5f23c7332670caa754f07691dda50f9bf356c1e4e472092dbf322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294059221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8626bc0614c0a012f34871fc2c3da87b68b70d534e68bd91167dab1745f676`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669209475ccf588005064aec8b03f795116e849de02f62977a14a87f1ef3e90e`  
		Last Modified: Tue, 03 Jun 2025 10:57:10 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e327007ba9f9dbc2b008dd518ee88f8e3c0b86546422fb4bd14c3c2bcad52526`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 88.5 MB (88511057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c174f014e53fa9ebaa897c53a1d7be90efc354d246e758c6496eb142fc4c8c6c`  
		Last Modified: Tue, 03 Jun 2025 18:50:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97d0d536b6a9d287cd7498c8a2a3357caa7ea679498a8830597e34898269d88`  
		Last Modified: Tue, 03 Jun 2025 18:50:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:361df1620071153edbe99cb5796424b3e8845ff5edd9e38bdfaca857da88af80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd11fe912b3d8b605d94c87532da673c250ce1741d6023a870c64f3091b54c17`

```dockerfile
```

-	Layers:
	-	`sha256:6abdf832934cc00e2dc4c4eb53d5ac62d208218bf0505f035015652a7cd8e8ac`  
		Last Modified: Tue, 03 Jun 2025 21:41:30 GMT  
		Size: 7.3 MB (7329240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d3544a16f1d969ad34ecf9c15c65e1c1f0ef07cd58bb4105fa9106ca96b001`  
		Last Modified: Tue, 03 Jun 2025 21:41:31 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e2149556388d4becaa1dc35657a5706321c4e8686ca1e61e15e6d7cb8755b3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304837179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a03f581cc035150b90200f8a88409640b4e91b2df80de33425c3e9286ff04f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f6bd552c8941351aec1fc10e7be3cba78443c32cad3ba1481c6ebefe465a52`  
		Last Modified: Tue, 03 Jun 2025 09:11:02 GMT  
		Size: 157.8 MB (157804856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b61c04060a68e4f861233e6aa44907e4c977d252ad139304736358bb36ce91f`  
		Last Modified: Tue, 03 Jun 2025 19:07:08 GMT  
		Size: 94.0 MB (93950738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db78e52de32a0b285a0ef7d1c5c69ecdc8a23db606741509f7e5dd10afe2b56c`  
		Last Modified: Tue, 03 Jun 2025 19:06:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0064d7dfcc9aaca4d8eee07a937c89b2f2a531c7faf67a17bd404bb086d961f6`  
		Last Modified: Tue, 03 Jun 2025 19:07:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3047ed82b174d4cb429fb38c933280023dfd76ba28bc45cef585982d3726570d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7343140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ce196f9a783e3a30a54865a6811de5ed693bc3805cd5b09cc729939198704e`

```dockerfile
```

-	Layers:
	-	`sha256:3eaace5a72ce7464ecdc541584c85b6c7cc9a112f51181287dfa50a18648deba`  
		Last Modified: Tue, 03 Jun 2025 21:41:39 GMT  
		Size: 7.3 MB (7326615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76b3d5dc66fa881586ba062fd0e8ecd51e9b02230f56cc7ff39d76ca468d3f1`  
		Last Modified: Tue, 03 Jun 2025 21:41:40 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:00224c6228a0779f0d43a0ed0b3ad7633fbea6877d086772d9a2a6087271958e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288037772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81efaeb6bb424b5c064e1a0554bda493b739251c3f18a511c95e6f8bbae90a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df655a63a53f1eb7344d055b3a0a02078ae226dc1a077e6b3a1117732b72b764`  
		Last Modified: Tue, 03 Jun 2025 09:38:50 GMT  
		Size: 153.4 MB (153449622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b509a4a82e5518079103db459c9b892edfd7889378deeff2a6eb645e8d24f13a`  
		Last Modified: Tue, 03 Jun 2025 19:00:59 GMT  
		Size: 86.9 MB (86855696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d423a80a641b585765f9b56ca76b369c6568e81f77c04d4e6b0b51502dc0478`  
		Last Modified: Tue, 03 Jun 2025 19:00:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d28c39f3d64ddb417af35460d807c69ee5c2bab0ca4021f7ff8fa703a00ad`  
		Last Modified: Tue, 03 Jun 2025 19:00:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5da445650a64519acc6896a586ff7c9efdfc230b7eca57834da1665f3edef575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4606d50f26d500b6d4160fb04b7c0258dceec801066cd5c2c43222543126ae96`

```dockerfile
```

-	Layers:
	-	`sha256:42cd2c431fbc992118b829347b784ffea95ce7deb8a371c732d061dbc363ccc8`  
		Last Modified: Tue, 03 Jun 2025 21:41:46 GMT  
		Size: 7.3 MB (7310109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cff28c6adbe7404accb7a9a8117ecad4610c897b6e3afc9ca0860495e85a405`  
		Last Modified: Tue, 03 Jun 2025 21:41:47 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4cc8832e7326e3654b2071f71ca51b4013d5967be4a137ed417a43a62f8d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285186943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd520cf560bfe6c6b036798916a075daf711780c1e3c422d56438185ae7b2d21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861de86bc3adcdc8dc3323ae415856608e017573655a6d8e472b10aef094a90f`  
		Last Modified: Tue, 03 Jun 2025 06:28:03 GMT  
		Size: 146.9 MB (146911014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d8f26dec31d90db90070c5ba6cea64fe5dd5de50159bfacc617dc1f8d66b1a`  
		Last Modified: Tue, 03 Jun 2025 18:41:54 GMT  
		Size: 89.0 MB (88952662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42791148ff0249cb693ac3cfb7b6f057107df4d1f8767d00ffaf999e2c407bc1`  
		Last Modified: Tue, 03 Jun 2025 18:41:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29f1380ff7d7b33be17b9dbd80154755904c2cbc47f2682edfc8a462b0298a6`  
		Last Modified: Tue, 03 Jun 2025 18:41:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa92e07ef2f286c7bcc05733cf9be5ebf4f9029b26df445c39e7c39660d7cc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e88002c392f4f68049d360a742c56d0e4a14f0b1f12a1098251e1af226d6c04`

```dockerfile
```

-	Layers:
	-	`sha256:7ae6caf0f959612bec56919bd4954005f34a90c2137afc48bc64700dcea9673b`  
		Last Modified: Tue, 03 Jun 2025 21:41:53 GMT  
		Size: 7.3 MB (7318108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e89dd1353402b363589bf86f738bbb11246744caa8a743e68a11d5edb01dcd60`  
		Last Modified: Tue, 03 Jun 2025 21:41:54 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
