## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:487cb28a7e6b9abb28f8d17759b2b7594282e2229f5e1f8377210ac3b45eb604
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:730b8a1874f0bd0345ae3de812678a8b20757954d627d890b7ae0d9f46b0f0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189944906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1368558dd71cb4591e2e34cf3a9e4480675f1a7ebece36eabb3aebdf30af4b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:56:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:32 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:32 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afce66202401d23e859925065088050830475bc2154a62615ed7b2e3992a035`  
		Last Modified: Tue, 04 Nov 2025 11:49:51 GMT  
		Size: 92.0 MB (92036035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a0608f1adf5b2ef8e801cfa14e7f70e5782fe8388f174315b6ac2fdb29e677`  
		Last Modified: Tue, 04 Nov 2025 00:57:21 GMT  
		Size: 69.7 MB (69679267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a510f64ee23e193a193ac2bfcf5ff3d4b81ff718de899cefbe2bead7a689fa`  
		Last Modified: Tue, 04 Nov 2025 00:57:13 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df91e21a706ec84d6c9d250b5afb3b804b700f1826b9bfd79eb1bcd0e461130`  
		Last Modified: Tue, 04 Nov 2025 00:57:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ce58a388bbe472ead8e780a1a074ec899c4ec4b40d03a019096bba205f63b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b41bb1d7817323c61099b4962c4c4c20fb75cb2de8cc5908c0334ee587b5320`

```dockerfile
```

-	Layers:
	-	`sha256:11510089b9a49b0b3c6fb474e95b41a07e9f6308308dd4b4f19348841dd46cb0`  
		Last Modified: Tue, 04 Nov 2025 10:45:30 GMT  
		Size: 5.1 MB (5064734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d023ac8828b66fad073bb0b6ee95d286c175687dd65eb441c9b1bff344c5e5`  
		Last Modified: Tue, 04 Nov 2025 10:45:31 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:743c8594898ebb92f9dca738a7bf831c3f88c7f0d39d2bb2ecd0e85f06a6aa08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188709067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7f038f6dd1c4d7943d9bad44be83a6dbdb998bbd4b33d40feb2a6b85db21d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:57:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:57:20 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:57:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:57:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2391301fa160ad71751a5ffef5e12f7be7af65b9d47337f1d1d682e8687b83`  
		Last Modified: Tue, 04 Nov 2025 00:58:14 GMT  
		Size: 91.0 MB (91045229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3df0e661d6387ba9cd71eb5594044308e6c69312419167b749b7d0521f4f6ac`  
		Last Modified: Tue, 04 Nov 2025 00:58:08 GMT  
		Size: 69.6 MB (69560420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fc25a5c9bccdf85a89f0b70fe69f8f0af6b8dc16291d2a90ee82e0ee675b8d`  
		Last Modified: Tue, 04 Nov 2025 00:58:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1831f7e6765a14da57d6968b4aa60d96b412446bae6bc38802d0a35a558d5576`  
		Last Modified: Tue, 04 Nov 2025 00:58:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb7ea5fd5e6ccc5d1cdb48482a6bd74cd88e5cbcd654b7f1114beb0193a60cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f551463e263d1e6c97b1c3fafa9b288afa1a49c3aee9fb5d1f3885263900d7`

```dockerfile
```

-	Layers:
	-	`sha256:0fdfd30d7510a29422834cecdc93561c68f0e4b853b16d94f60820b3f6ca0dfc`  
		Last Modified: Tue, 04 Nov 2025 10:45:36 GMT  
		Size: 5.1 MB (5070516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b414f35e2d78848bbac0dc7da5a4da5f6936836b3cfffaabd0bc8f4480c62d`  
		Last Modified: Tue, 04 Nov 2025 10:45:36 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a823c90fbeabd1d8c76303a5d1b6e4f5c7c7e8edfb45a2ce75893d8e8b17f265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199184977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122c429a1ac82d9e6409929456776649a93072f591947c1366a74f7a77e8c12b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 13:45:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:45:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:45:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:45:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:45:28 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:51:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:51:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:51:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:51:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:51:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0c2cf067a522d102e8a45c8b4182799ef8218996a3335f677cd91f3f335615`  
		Last Modified: Tue, 04 Nov 2025 13:47:05 GMT  
		Size: 91.6 MB (91601696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3a9fb3983fbc8c1ef281b866d961942e17d543a942ee880e3dd79768bb189f`  
		Last Modified: Tue, 04 Nov 2025 13:53:29 GMT  
		Size: 75.5 MB (75513334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c002bccedde9830e85de608bdf2547889a3f4a95b35f81be60c435c8f353aa14`  
		Last Modified: Tue, 04 Nov 2025 13:53:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03522528fc222b1fc828653e88efcaaf862711ae4826e1d1e73159d8bcf00e50`  
		Last Modified: Tue, 04 Nov 2025 13:53:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:497ad21d7c040758f44796ecf9b708248379c4aeb6a6fa7139bc0a6f6bb7730f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c41673adee23c145edacbbada7dadbab099d694651295cc9407d47b7b5b1a`

```dockerfile
```

-	Layers:
	-	`sha256:c9380068709044cacf196db8ece406a585c115b460cc6f371afb3112e528f76f`  
		Last Modified: Tue, 04 Nov 2025 16:39:27 GMT  
		Size: 5.1 MB (5071202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586cc28abfb1da84c0fc624984aec4a19b27cab23f4633347e59f1f64568dd7e`  
		Last Modified: Tue, 04 Nov 2025 16:39:28 GMT  
		Size: 15.8 KB (15786 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:67e342641a17c37bfe4501a090839f95cc8b567cf62997689f32a56fa87e9ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183582757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99753c3b1fd77fe7c15aabc7472f117d515f0fe4168aa068cfeb04097a1e9c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:34:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:34:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:34:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:34:23 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:34:23 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:36:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:36:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:36:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:36:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:36:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a63620f6a8e2b1330d73d22de0846ac03745875003b79f479fb5a39f9a2684`  
		Last Modified: Tue, 04 Nov 2025 06:35:10 GMT  
		Size: 88.2 MB (88206427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f21033bed3de190df21f6e449063807c418a70b701a8103c2d680af9c82f5`  
		Last Modified: Tue, 04 Nov 2025 06:37:20 GMT  
		Size: 68.5 MB (68490736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe21f1c2ba88f317bba1b9c568d1501dff608cee7c3b81c0d0f89ee091faec22`  
		Last Modified: Tue, 04 Nov 2025 06:37:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b90b115544112ba7acad3f7a7296de2fb2e47eca1128db74a134abba26a3ea7`  
		Last Modified: Tue, 04 Nov 2025 06:37:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a30612f3314e560d8423f5ff63d53d958bbfc9d8b76f29a4aa4888b37f3e4de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148649ee73d5aafcbf7bb3fc8ca8b48523d35a7835a22859984ac20a1c6c4f53`

```dockerfile
```

-	Layers:
	-	`sha256:c01f14b290d08a02faf6de1ddab12ce0ae4e335221656385eb2a2e147e4f9cf4`  
		Last Modified: Tue, 04 Nov 2025 10:45:45 GMT  
		Size: 5.1 MB (5058603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16403b048c13560e96f37cd07856d02f95882ea9ec408791dd30d0e5e3a0389`  
		Last Modified: Tue, 04 Nov 2025 10:45:46 GMT  
		Size: 15.7 KB (15725 bytes)  
		MIME: application/vnd.in-toto+json
