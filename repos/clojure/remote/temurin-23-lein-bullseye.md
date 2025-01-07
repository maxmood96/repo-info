## `clojure:temurin-23-lein-bullseye`

```console
$ docker pull clojure@sha256:7b414f87c91c3af60c2061f4e6241f7d4604719f3f9c4df162d0e0311479794e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6e6cf4f8dafc020dbf6fc9234152ca8feba3ec81f7fc66b1cab1a4a4990b80ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276126953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4055440dd5a79c7d701d8a1e87d07294b365e2bbf1fdc4ff891f29958273d9cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2403e384111eb93c9561c8f5a6c45cb953d6ab74b744c597efa514734e295db`  
		Size: 165.3 MB (165295091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f28524b1db4f01c512dfd36855ca03725f3053e694573eacaa951f3345ec56`  
		Last Modified: Tue, 24 Dec 2024 22:38:53 GMT  
		Size: 52.6 MB (52578283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abf3a35dc8da8f4f531d543cffd6591b9d2f142998702ea790563c9b0aff393`  
		Last Modified: Tue, 24 Dec 2024 22:38:53 GMT  
		Size: 4.5 MB (4514194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef10f4ca96014183fae0e16195508cf6a432466fcd915fa8363e7f496d888df8`  
		Last Modified: Tue, 24 Dec 2024 22:38:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2b05c941087aa43fe020fd393706cceabde42b0255baca26c7d034aad70fb3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d649ae24cb7cdbde433d8c89d162842f9aec91a086fb8e52edfadef7d96e521`

```dockerfile
```

-	Layers:
	-	`sha256:c8278c422ca4c26b2c7704e3b48e5894288a1b901d3b4b8082d03c621c9d78b9`  
		Last Modified: Tue, 24 Dec 2024 22:38:53 GMT  
		Size: 6.6 MB (6624763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13cc408bbdd677a95da01252d1222f3866d6cc4dde02d8aa1053213f8f637d38`  
		Last Modified: Tue, 24 Dec 2024 22:38:53 GMT  
		Size: 18.4 KB (18422 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eff6aa9597caf31d78d7f89db7e95d06537c99439c55dccd75f3d3f4a06cc017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272666652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6dffce3bde83bb8f208470725ad22a81f2147be86958be626b7f41e0e3cf41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6695db2a9af9c621e2afd751a22f972795b62d6695e9f4d372982636e107ce9`  
		Last Modified: Wed, 25 Dec 2024 07:38:55 GMT  
		Size: 163.3 MB (163281797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11d8d6e51d59d463fc99cad735c99db6889c8285be76d3279e1ce7546b13a85`  
		Last Modified: Wed, 25 Dec 2024 07:38:53 GMT  
		Size: 52.6 MB (52624584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97f5b777a6558ce55909875ddab60100c2eb386925a82865872f558e6f417b1`  
		Last Modified: Wed, 25 Dec 2024 07:38:52 GMT  
		Size: 4.5 MB (4514145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670dbd498554cec6cf5be85a138ab1a6cefb3d546a5184e03ced98ef04499dd8`  
		Last Modified: Wed, 25 Dec 2024 07:38:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b1cf2fb43995b0c4218c5aad88b25412b19059be69ccad384b3394b86dd89418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de752281500d278b4c9cfe981ab5fa685d66a02202f34250465bb738adbee8f4`

```dockerfile
```

-	Layers:
	-	`sha256:fa47760a6d1ce3332d8aad64e600ed571f19ffcf4a8035633f346e2760b700f6`  
		Last Modified: Wed, 25 Dec 2024 07:38:52 GMT  
		Size: 6.6 MB (6629173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28aeb25a15838f19931278c226af720f3f10337b3bfa482417e15d90c7d38db0`  
		Last Modified: Wed, 25 Dec 2024 07:38:51 GMT  
		Size: 18.5 KB (18543 bytes)  
		MIME: application/vnd.in-toto+json
