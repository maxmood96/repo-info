## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:077b6ca12bce04634e34a9557c58466ae533e17f20354447f6aa575fda3a83d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b9581258a031380b896961747237facce0cf737f7bf868840e8598b4aae87828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242602465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8583e8a8a4a6b5b8b90e9db7affb7503b8505d61678a531202dee185d25aa4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d7f3cfd4882825aa2363e457327ec70b94ef6ad3f1a99bd863819ef581407f`  
		Last Modified: Tue, 30 Sep 2025 00:53:49 GMT  
		Size: 144.7 MB (144693609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d064533641562cf6768d9414f114eb845afb2dc7cd7170ede40ee239c6a308`  
		Last Modified: Tue, 30 Sep 2025 00:54:20 GMT  
		Size: 69.7 MB (69679476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d343fd2000f234da8fd515843b9e0b8bedb8920c78aa360a1761e79373a532c`  
		Last Modified: Tue, 30 Sep 2025 00:54:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be4452ad08efcd7ed7f6a13efaedc35df37cc5cee5cae0a8e42a440f6468a18`  
		Last Modified: Tue, 30 Sep 2025 00:54:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c950fe6e1b7e50c6c11817731051af3c675e1a0cf56b9b23f90c25e31ef9f836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8a22645e2b333c3fda57f21f60590cfa452eadd16bd783f6e90b3a7c5e2ef`

```dockerfile
```

-	Layers:
	-	`sha256:3e0f6b916e7cd2e30403dd371358726be43adfbe7b0d0e12ddcb832500acc500`  
		Last Modified: Wed, 01 Oct 2025 15:37:27 GMT  
		Size: 5.1 MB (5113388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62884c7ba201f9143b98061841dfe2ea58f3a0649908e03a1b2dfce26bf944af`  
		Last Modified: Wed, 01 Oct 2025 15:37:32 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0538080b63510b2e28cc8444793347ccea0a4b8275134e7cf1448fd05e779c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241205611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a194d0c72dd30df166496ff9077cac58ef5412bab4a802edcf263bfce021a7e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a3fb691bad954d1a19d997963f948d0aeadc5d97501b977692f5a85e7e252c`  
		Last Modified: Sat, 27 Sep 2025 02:07:26 GMT  
		Size: 143.5 MB (143542147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cd7cf385c8941091b3b556b815a7d47fe5b340086bf89a427db25f900d8690`  
		Last Modified: Fri, 26 Sep 2025 17:54:34 GMT  
		Size: 69.6 MB (69560323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f97dc5b502ccb2e04ea24a5130f01c05a3c3f11506ea2275895db64def2a88`  
		Last Modified: Fri, 26 Sep 2025 17:54:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3888262e48760de1b71c776d09c2dc97e13ce074aec285843eacd809e051fb7a`  
		Last Modified: Fri, 26 Sep 2025 17:54:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:408b0b53ab959cdcb39dd15ba62e4f82cf159950721502bf687f0150d28e73ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e8e3f1a57263a51309be2ced7bd650960dd2273f891330213f55c7284915e6`

```dockerfile
```

-	Layers:
	-	`sha256:2bf22d41d56919cd55a01546cb875fdf73b459bf66a7717d19fae072b8cbc917`  
		Last Modified: Fri, 26 Sep 2025 18:38:43 GMT  
		Size: 5.1 MB (5119149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7e5cb5c25c14338736ac2581644e27f2ca78e1ea067146a9b65704afca5c3b`  
		Last Modified: Fri, 26 Sep 2025 18:38:44 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4a4815a113e5040c8383a6f98818fc3efcf39c61bc3d9cb1f301f527b0dfcc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251955963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884237c0a33501dee4bf8effcae0c7ee7a58ae42eaeecf0a4bbd1fc779f3fb48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e4a609299433ccda31e3a0bc9615c82f8e63ed1cd9782670fb94f179ce6066`  
		Last Modified: Sat, 27 Sep 2025 20:13:21 GMT  
		Size: 144.4 MB (144372862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e8a344176fd32dc2be8654d48a5e91ad82a927eb1eea6ba1b74199c3bc3a1d`  
		Last Modified: Fri, 26 Sep 2025 18:15:14 GMT  
		Size: 75.5 MB (75513299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0584142e249b3156f4a02371c18ff83cee21679a8b3a926f76e45fe29d263fa1`  
		Last Modified: Fri, 26 Sep 2025 18:15:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988f9e53ba2b9ac732456fe7ac596fa35c6c7f45c4e5d9c89d99de046cb901c1`  
		Last Modified: Fri, 26 Sep 2025 18:15:05 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e6e97ac4403221a0e8222882832ded292489d748b0597af47a562b66a16ae9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c36be7f1d0caeeff58f3b96a8c3a7e82aa88590e2bc92e75f6a1701525b4c24`

```dockerfile
```

-	Layers:
	-	`sha256:31d5b0c7491ba99e1d72090b91329f07eb2e513e6a0a746412d92845b16713c8`  
		Last Modified: Fri, 26 Sep 2025 21:37:15 GMT  
		Size: 5.1 MB (5118546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bd3c2fba46a8ae00b6fdb57bea64f24e8d353629b37a5bbd3ba61ce2530a78`  
		Last Modified: Fri, 26 Sep 2025 21:37:16 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c7f680040890275dc1e33b45a8ab480055d1597d89d50c671c941b7e91bda925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230100474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ed3e3f9ccd981e17b16d83d2737ab42bf994fcd01874a545a24d9281a92cf3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817ac40e5124baa038fe8a6edd50ca9606fe083dd19116937a1579559685efa7`  
		Last Modified: Fri, 26 Sep 2025 19:03:36 GMT  
		Size: 134.7 MB (134724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25605cd72e53c1848e5cbce713b747d32df70683cdf2499cff1184bd0671e4be`  
		Last Modified: Fri, 26 Sep 2025 19:04:10 GMT  
		Size: 68.5 MB (68490799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e238b4666ba1bf4c9469891a161e5210d5d387996d5c8845ed20d479ae48dd06`  
		Last Modified: Fri, 26 Sep 2025 19:03:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00eef9615106607b0a3880ed4d1e73013f098d065fe278f27a3199557bb7271`  
		Last Modified: Fri, 26 Sep 2025 19:03:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd01b63e1a6733e6378ea6ca6835310dbb0aa4fd966d0740ccc44b22b2c65d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b084a39369f2c32e1b1d7fb38fabf11290dd849c47459a2c00dff562ba52a`

```dockerfile
```

-	Layers:
	-	`sha256:cf74cc653c03dd5d409f2ff904552f6b04f943d1a0474f94b69213a1db76e541`  
		Last Modified: Fri, 26 Sep 2025 21:37:21 GMT  
		Size: 5.1 MB (5104709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d586189f12f3cc0c157050755aa9f682f8a6eb7fc12844e28b179895840acaf`  
		Last Modified: Fri, 26 Sep 2025 21:37:21 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
