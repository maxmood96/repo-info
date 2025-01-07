## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:6f2f94dc0b051f893bd2301e2a460a2190afa85304737f7527cd6cc974a4f924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:277dcb5ed57666715bf5245a82a1f4bd0360789a5ae600b3c59ab59204cd6a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267436677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6adb657a6049c56a4943de8b99385b22fd6ea0eb31c56ee23240661990c9ee0`
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
	-	`sha256:50cde9188f35989d4b59cd78defad7e0b91e90e8e6f8932ca8792ae53ea63191`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 144.5 MB (144536666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fa4cc9ea238fda6fca5e1c0ec4b630245aa3c06e13f0cc3a00275df9ad766`  
		Last Modified: Tue, 24 Dec 2024 22:38:28 GMT  
		Size: 69.2 MB (69160015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b172720149e92d5f3cd3063a8da39d1a68647a468e3d1b78340ad7626e2223dd`  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25a11a8be72a9fa8d0a3d017d1063015aa8acc1b026345a7cd9d32f61fe31c5`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:58304f9ddb155376ff3c954647ce818ff01b1a7774f58f5b57154bd3a671adca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7465076b46570ecd7ab04159d308768193c4f2ed1a2342fd9a2e12b4dc5037`

```dockerfile
```

-	Layers:
	-	`sha256:8c58bdf3200e50c58bcad72b3562c4492debdff848f59d91f7a22bb0d7212f09`  
		Last Modified: Tue, 24 Dec 2024 22:38:26 GMT  
		Size: 7.2 MB (7204495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd704be2275ec43bd1dde9161398a0a8f813ff5a0d5e34bacb2ef719cb50d04`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec1b5f1d1f5a525a87e58ad0cfd651e54a9810046b905568bda945d403f0d022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264893269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f633b1345095fd894e4fc62164330f4e7e2317d54041754e1a8fd3a109d599`
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
	-	`sha256:8dce462c22105422e138f6d754df187041f54e682066c38e939203fda7d53c73`  
		Last Modified: Wed, 25 Dec 2024 07:26:24 GMT  
		Size: 143.4 MB (143360983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249bc8bd38c44cdb6d17eb93ef60bc5a9bff43ff15bd04a661dff6755827ff1a`  
		Last Modified: Wed, 25 Dec 2024 07:29:22 GMT  
		Size: 69.3 MB (69285549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a453e57d237c83cff4ceaf6415e7b4ad008dee39e3bd2d3ec2fe5cd7d35ab055`  
		Last Modified: Wed, 25 Dec 2024 07:29:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b2daf49ac3892cd01e6881fa23da87b9166e1a9eb44cd598f6b046693f4eb`  
		Last Modified: Wed, 25 Dec 2024 07:29:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:85de4e2d913a2092764d562c1394e74fed5742d65b826f21f6485bbddb19437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9073a5bacecd9105b1cdb5c13d1c3664492480f7ef2d7f56022fd7b73817e6`

```dockerfile
```

-	Layers:
	-	`sha256:9cfd9ccf7f90e0aec6252774dccd077bce66a9d591a3a9f551ee54c2d9e4c86e`  
		Last Modified: Wed, 25 Dec 2024 07:29:20 GMT  
		Size: 7.2 MB (7209594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc2664612b8ec8d948d462ca20971630d223e89c27d898b6d6ae5bbb98bd30e`  
		Last Modified: Wed, 25 Dec 2024 07:29:19 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
