## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:6215b11f3dc50c14807bf17d3828a0c96de51b0e6af4cbbbe5705359f7bb419d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:08ffdc2f011f883a4c899c18f86d2e4ae3d7e137e73c618b9614785bc08031aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233883588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df19048c227a29d094863ed88a0cd27619ca3c5d2309f80874f5194fad7bbcd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64605cff81b40473d8f25896ec2723ba277d28b3ce896766fbb1321c6c2c7f69`  
		Last Modified: Mon, 28 Apr 2025 22:07:32 GMT  
		Size: 144.6 MB (144634946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcdf2bc0df5a28f1e3e2975fc8c8f6cf16cb8f9b1dee9b66e5a81aa8fe4ef7d`  
		Last Modified: Mon, 28 Apr 2025 22:07:31 GMT  
		Size: 59.0 MB (58992998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f963ce4a357023d3ac80219020c9a1cf7ef0156275b058ec55a83780280006e`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21f5afcd69ec7c3752023c5a1c518fe127adc91a3c95cb123090cc116adc26b`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9f7f89a61b9162356575a564a732c1175fd9ee9fc4c4a794796a30b138b1bc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09159c9ab2330f171167cb5666dcb7259cbbb17135ab83d1069af1d00177131`

```dockerfile
```

-	Layers:
	-	`sha256:df9c5908db7030fb75fe174170b5718e6ede229f4e165eb479ad7da640fd45b8`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 5.1 MB (5119067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96aa38c2f67cd0c825ee0e55c7d12dbaba94f556fee458149b9cd78e0643aeab`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:495cdc0f7de38ed1fe103f278c244b33f7307674b16a9307acbeaab47d15c2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231390582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6aee095cc9a44da0360a74e54ba1eae6adf25d67c554dde438707de2a4cbcc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2cbeb7de91ba4cd7ce2a6c214ea30fb41267c58cd7905c6d012910d146e1dc`  
		Last Modified: Wed, 23 Apr 2025 18:11:47 GMT  
		Size: 143.5 MB (143512631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d753b9fb28ef2345607e63e3affad49186aa078d9323f250f863076b340c3f3`  
		Last Modified: Wed, 23 Apr 2025 19:52:07 GMT  
		Size: 59.1 MB (59127407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed575051da99c77253a3c75f04f35a4aecbf4838e3dcd95e88f117a4168a0e8`  
		Last Modified: Wed, 23 Apr 2025 19:52:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623b1a9ddb099346023b2b779f4c60dd36835bfd24e9e0e1e9cd1c9f8b66048e`  
		Last Modified: Wed, 23 Apr 2025 19:52:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:739b999aaabea659e27032f021e8685b68664046def2bd4eafc390df161be507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3a33bfe141099028f5ee954661e4a055419fd5d016b02e207c49af6863d144`

```dockerfile
```

-	Layers:
	-	`sha256:17baf219f7873f9cd286be6eaaf26f5ef40632e67c716605d9165e06e6ddda18`  
		Last Modified: Wed, 23 Apr 2025 19:52:05 GMT  
		Size: 5.1 MB (5124745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42e8a65eeeddd52c013bd9d7f4d9e840561c38acecb70b51706606dc0590ed3`  
		Last Modified: Wed, 23 Apr 2025 19:52:04 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
