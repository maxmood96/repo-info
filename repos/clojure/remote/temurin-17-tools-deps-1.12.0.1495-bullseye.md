## `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:3d3b8540701c1ea2eaac3332f41870063bd69575dda6afd8a435f77d11e61b1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fb61d8d21014454c379e313263ff50bc8b149cbb672812d7cbc1e2ffe2bfa26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267455279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21de510fac981874848a641870b65b8f1df3cce7824f1024c473d6db551c30b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ae37c2de7981a04e37b5c02fff0674f8d2681b71d719105f02888b5f30cb7`  
		Last Modified: Tue, 07 Jan 2025 02:29:39 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dc5fc99097e7148c54775ed7a654db51ccd49e61633ea553909c298140b647`  
		Last Modified: Tue, 07 Jan 2025 02:29:37 GMT  
		Size: 69.2 MB (69178567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bafe454d00b7fe7ddaf1c06f610dfdeb0feb277b6b0c3a50f76d2a112b24b46`  
		Last Modified: Tue, 07 Jan 2025 02:29:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b7367cba475603a4b926883ffd9024ae49ec06f10c21c135356f1ef804f7f`  
		Last Modified: Tue, 07 Jan 2025 02:29:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c31aa89e7726756ece6b24bdc7dffd77619acf4c565ba9c3487c32cd871d34c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2486998bc58deb0e9c121e01a44e1f36297e4ece52d450aa827fc88cedad27`

```dockerfile
```

-	Layers:
	-	`sha256:75736b5463afc8887f21435061eb53faa15c29e338ee53a99c3e1e7c2b68e04d`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 7.2 MB (7204557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9aafe4610aca6d5d9d518d348e18f4f6fbad9c18d4724cea7bc5db1416bc067`  
		Last Modified: Tue, 07 Jan 2025 02:29:35 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a103a7d45f404e54074c51bd3b933b88a91f0b1929faa6f9c63cb86ae94e04ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264912195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61350bd5d4601b97b494644418da17d00b7fc4ac386bb9d9e36edd3a3aae2eab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Wed, 08 Jan 2025 04:45:40 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dce462c22105422e138f6d754df187041f54e682066c38e939203fda7d53c73`  
		Last Modified: Wed, 25 Dec 2024 07:26:24 GMT  
		Size: 143.4 MB (143360983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f37e36813eb806137f72237dedf4c41060ef4eb6f261b3c0ac28ff992f17e0`  
		Last Modified: Tue, 07 Jan 2025 03:28:28 GMT  
		Size: 69.3 MB (69304472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89e883012c075fdcb3fea7e6ca99a20201560220fa8167a996d67de756f489`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d0e43d7f4889e2b0469023202ab310790fce520374a4c03a7e5747b92af65`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:814b09ba400a040f3079eb898d304ac920eb84f8fe3a3613a48c633cd10fd7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c4af2bd9a51896d44115e90c058fe85c91d6c8f34fca1c87ace3c88271dc1c`

```dockerfile
```

-	Layers:
	-	`sha256:400503bc0a24f89c5148b96c4b0b90d9ed46b0345491cadbb6f7b6e14b3bc18f`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 7.2 MB (7209656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab5813db75de4d975798276ad4ed4bd2cd6e8343b5ff70828e15529ff8211d1`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
