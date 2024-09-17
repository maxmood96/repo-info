## `clojure:temurin-22-lein-bullseye`

```console
$ docker pull clojure@sha256:f03012ac680589be8a5601cace3cb1aa14cd404bef74a431e4fea22e413d7690
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d6ce1968bdc480f330b437f64eff228c5c30e0496105db47e8f7eb50b8086622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268858884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd79fb6ae7de429f4b7cfdbc99482d5ce919947ccc83fd218c02182bf397c65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_ROOT=1
# Fri, 06 Sep 2024 16:59:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f6c29c4ea598c3e9e0162aa1162c954a77be00423bf0f347267585eebbd216`  
		Last Modified: Tue, 17 Sep 2024 01:59:08 GMT  
		Size: 156.5 MB (156481658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762fcf3609fc8924da59ef978580d175f3ab61e8025ba6cd71f4f0d42fd8501f`  
		Last Modified: Tue, 17 Sep 2024 01:59:07 GMT  
		Size: 52.8 MB (52781328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b250218a82f3db5c83db26b89b00cbd1e81d73867906ad840cc80d14184e0d`  
		Last Modified: Tue, 17 Sep 2024 01:59:04 GMT  
		Size: 4.5 MB (4514139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfb1b4da0edafef03f3248038d88d761f1f8bcb398712fc9f32caaa6a7ec54b`  
		Last Modified: Tue, 17 Sep 2024 01:59:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4ff2728b997eb9f2c636ba3840551a7ca4bc909d5ec886e9b532c71dc55a3188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6474691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1838ac02254a8bbdc81540970daf7e3a0323741d82f5087fdee0871ad498450f`

```dockerfile
```

-	Layers:
	-	`sha256:6162cf0979c55267a813264bd99283c371e8dd914d03daecce3cb852dd805ea1`  
		Last Modified: Tue, 17 Sep 2024 01:59:06 GMT  
		Size: 6.5 MB (6456649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f75b43754e787352a48a84f5d8b0fb1fae8e13d651def42d6e0a4cd2207d8d`  
		Last Modified: Tue, 17 Sep 2024 01:59:05 GMT  
		Size: 18.0 KB (18042 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1cf43c8f3f4876ed4ce6207adc2f4c29a994ec3eb98491f040c8532ff69d5305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265570199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d17446576834963854417e585ce664f1b0db230bc56559767f8de4f222769e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_ROOT=1
# Fri, 06 Sep 2024 16:59:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b373f6ff7665f36b6975c9640d57de81ac735f9d9d471698a770405ed8e4253f`  
		Last Modified: Tue, 17 Sep 2024 04:53:53 GMT  
		Size: 154.5 MB (154503778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5d813381fe80a5926c80c923c52338dc3b230ce503cfcbe76d29402d7ee8f4`  
		Last Modified: Tue, 17 Sep 2024 04:53:50 GMT  
		Size: 52.8 MB (52820221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b2ddad33f76e4a7978ddd04d372ba5c5d3ab2da8d68a061698a95a7a981c5f`  
		Last Modified: Tue, 17 Sep 2024 04:53:49 GMT  
		Size: 4.5 MB (4514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b470ad842ad42ca6d3f721d5213ce85e66c34f6140d33c5156dac46abcdc99`  
		Last Modified: Tue, 17 Sep 2024 04:53:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:deb1f401dd2ca7819ce203ab29e0a5cd409d20142b5cbd49e6e0d78d83946526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6480869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6bf6d21828c5db8b31a2c82e018bb8670fd9bd97f1226a65459c79b7980398`

```dockerfile
```

-	Layers:
	-	`sha256:1b9be0c0c77cfd317b9e200f291c9874e33c13b139072d37aa1e1942218dc8c1`  
		Last Modified: Tue, 17 Sep 2024 04:53:49 GMT  
		Size: 6.5 MB (6462303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ff34903d8a433efb394e3eacbcf62672f283b05a20e8888b3d4efda8c6bdcd`  
		Last Modified: Tue, 17 Sep 2024 04:53:49 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json
