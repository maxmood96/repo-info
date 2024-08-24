## `clojure:temurin-22-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:f00cfe1170ea71b408574adda5933f632923ae7a4bc5ef5a6636fa010f7bb52d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c5a2af88a16a54507d69c69e60cb0ef864c571f73d1ea89cd2634b9fc469cd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241227244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809126d3bfc5c6f641350e215b9ef5df101839104e62f56fe6cdbd1902df6746`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44a584cb92b18942a7f1391e6d57bcfcdf3155a0a3cca817459d28b62a0731a`  
		Last Modified: Fri, 23 Aug 2024 20:05:28 GMT  
		Size: 156.5 MB (156481670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901e48acc47ab417f923ee1b411d0453d4eaf2565cb5069b8870c21f4fb8d4f8`  
		Last Modified: Fri, 23 Aug 2024 20:05:27 GMT  
		Size: 51.2 MB (51220879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543779d7f6e68603094a3639cf7ca76091b4f927d364f96ad8d81c43c6bd3801`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 4.4 MB (4398034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77826fdf700cbf4907a8ccd8f19453003dc4a85029d656d771af94ea564d627f`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6fc4f9033c662bb5219a59b26df1518c26eb52b1b57bc405b3b08bfd3013b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4765a5a69874c6313d575a3eaf798907fd77fe2a927b0cd519e5811a3a820b1`

```dockerfile
```

-	Layers:
	-	`sha256:e1b11de1417e33b564da3e2ea57460fb921ad33e6d3260772b1e5202db4cbd31`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 4.2 MB (4153003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4557bd6d3fa629e63a77a3328dec5afdda427c305fdfa9f9a8bdaa7be243df`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f9c667c2607f960808b0896db310308f582ae7a5814ce289b65eba1ab9b5855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239154111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fd155ef3bac51bdcd529655b8854a0681bff83542e2b2046b924eb19974293`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1fb39c7baa693f1d90f06cdeb26f0916fed34db00c7e3c5e300abff9ca8690`  
		Last Modified: Sat, 17 Aug 2024 06:34:13 GMT  
		Size: 154.5 MB (154503738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b796df8ec8f0e8e67fa204e48cda1c027e158d30348ef23532736a63a94b8e85`  
		Last Modified: Sat, 17 Aug 2024 06:34:10 GMT  
		Size: 51.1 MB (51095364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6998705e46bfd47ce1efd707d403e0e99cb1ea594d628606f5fcc00ebbaf09f4`  
		Last Modified: Sat, 17 Aug 2024 06:34:09 GMT  
		Size: 4.4 MB (4398051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180fd81f88f2b7aec3a25882d7af41f70c712b8c8200df0f443ab4a59b16cf30`  
		Last Modified: Sat, 17 Aug 2024 06:34:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1b88710f9d774c0e32aeee2bc89c87db957900ff61b51b8ee09c4d9b67beafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6060ced8b1bacb0915a8013f3da34bdc08713b6a431d4b78047979f881b4d7a5`

```dockerfile
```

-	Layers:
	-	`sha256:6eb3eca7a7e552d45134c144f5a8cfa966e7f31bb84c2706cfbba0ed28c7b862`  
		Last Modified: Sat, 17 Aug 2024 06:34:09 GMT  
		Size: 4.2 MB (4159319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad99de6ad2357bd7e8fd9c4270e2d643e38002df2a5c83ebfe6dd06965ce7e2`  
		Last Modified: Sat, 17 Aug 2024 06:34:09 GMT  
		Size: 18.6 KB (18621 bytes)  
		MIME: application/vnd.in-toto+json
