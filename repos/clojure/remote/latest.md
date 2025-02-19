## `clojure:latest`

```console
$ docker pull clojure@sha256:2aaaa535bf5e86eedde8ee1048cadf1da71459805b50776fe831f88d3002ee4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:6c802337c3964126f9c21f355b4563dfb7d7dcfadd8d70acee699c61be89be08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301214023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb4d22c57964fb35368e6efcb1ea1c4847ae80576ab5f0896ff8e684e233a5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75341b27c02074a4360af5b771024ba2b259f8505380ef017bcae016b187062`  
		Last Modified: Wed, 05 Feb 2025 16:59:27 GMT  
		Size: 157.6 MB (157585891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3ba3d30934aed8daaa7a48743e5bf1820ea1c871ff46fbc8e6139008011c6c`  
		Last Modified: Tue, 04 Feb 2025 08:59:10 GMT  
		Size: 62.1 MB (62067708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35ab74e478db41dbd561205ba637da29416e3e18b88271df74ab27b105d3f24`  
		Last Modified: Wed, 05 Feb 2025 03:43:05 GMT  
		Size: 4.5 MB (4514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd33a5674b95b3499941aa3cd7965d21a117e0c085f8f2346975384e2c50af5`  
		Last Modified: Wed, 05 Feb 2025 05:47:47 GMT  
		Size: 28.6 MB (28565530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5750bac87a33b927ed028ac75a95388e36bee55a928a8ba3ed90793148b39bd5`  
		Last Modified: Tue, 04 Feb 2025 08:59:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273917bcb3c4610834f9ecebd9bd9696c281b8682b3aefa706ba39244622707c`  
		Last Modified: Tue, 04 Feb 2025 08:59:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:db21918cd7d8a56c6237380b130bed091b212c920e4a5d94f84882bc16c635ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7273479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79d31f502ab403df36fc38dd3f360e485c3838ef39eb271240ee708fc06746`

```dockerfile
```

-	Layers:
	-	`sha256:f45f844391a00769e58b333fcd8c5a3870c5aee54de30c204b2765913c4de0dd`  
		Last Modified: Mon, 10 Feb 2025 03:21:52 GMT  
		Size: 7.2 MB (7247805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfb7014759b090b9c947dbdf531149c7b86212f3b28ca8dd13ea25e2b0877ab`  
		Last Modified: Mon, 10 Feb 2025 03:21:51 GMT  
		Size: 25.7 KB (25674 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c0b5c0a6ab01ffbbae9e8efd0448632b23bb25cea3f6d73ac5bd12c06d44d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299163451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e901b500cec9f7ccb06bd69a7ee32fd6666c73c7e2bc1d637223c8bdac2d55a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5fa34edacd0f0acb63e2f1d258d50a9bfe6e1592d31c38031a099fd6fb4fd`  
		Last Modified: Wed, 05 Feb 2025 02:01:25 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f9e794e07797e8a8a880cd4e68526c8adc60cc32d20db878e1bd23326f6048`  
		Last Modified: Wed, 05 Feb 2025 08:58:11 GMT  
		Size: 62.0 MB (62037561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155e2917382c531832cd0f87f7c53d2e14b584b6be37e97fc6ef4fc153c2f743`  
		Last Modified: Wed, 05 Feb 2025 08:58:11 GMT  
		Size: 4.5 MB (4514161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01523dbd6a5b5b1cdd3dc949069815a83cb29f176092ef65dd6e277797bd8ea5`  
		Last Modified: Wed, 05 Feb 2025 08:58:10 GMT  
		Size: 28.4 MB (28444830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae9d81c257183385f68ab8b61c3ed48f987ac75a65695a4e7d4091fea7b968d`  
		Last Modified: Tue, 04 Feb 2025 23:23:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb556b2787564faa824d2553f9338107ebfe31cea61f64e0b8a2b0042dd50e7`  
		Last Modified: Tue, 04 Feb 2025 23:23:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:cbb6f903cbaff92addf29d50fab5eb2a3ef7d5b1459978b9701b72bbea30351b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7279341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119ffc1b081a8cebaa66d297102615090dfaab79c94fe06beaf6f1a05ecddbc4`

```dockerfile
```

-	Layers:
	-	`sha256:bda433bb7855aa648e729956c0df5b63a31954aef65210ba9f7dd271ca1f611c`  
		Last Modified: Mon, 10 Feb 2025 03:22:15 GMT  
		Size: 7.3 MB (7253544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa6c41975268f096cab1171a5c92b3a1f70b3c3a486c641ff9af7e06aedd03d5`  
		Last Modified: Wed, 19 Feb 2025 00:24:00 GMT  
		Size: 25.8 KB (25797 bytes)  
		MIME: application/vnd.in-toto+json
