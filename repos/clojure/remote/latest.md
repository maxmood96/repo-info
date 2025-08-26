## `clojure:latest`

```console
$ docker pull clojure@sha256:fc75a04cd1476cc09f8fd7d9962055d4b1619cac204cd9a37a5823a616a43bed
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:955f512c43b5ed04c7812e5e5869986e8bbbc94838c041b7fede6340bfefeab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305467782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f30ab4529e5643db1e6db90f6f1d22e65ce037c869dc31b7d9fbe0625e1b37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea80b59194ba30241cc1080b925fc6e1b00e36e43937bcfaa8fa02b680d80c94`  
		Last Modified: Tue, 26 Aug 2025 18:35:30 GMT  
		Size: 157.8 MB (157804778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5138b81596efb506176f17e0e77ca641bc9e978b21b4d6cc11fb8a1db157fe2`  
		Last Modified: Tue, 26 Aug 2025 17:28:11 GMT  
		Size: 62.1 MB (62084473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aa72dc892ccde3348d54d10d7a73f4f9e30e21f96d71df01e91302ec35ef89`  
		Last Modified: Tue, 26 Aug 2025 17:28:08 GMT  
		Size: 4.5 MB (4514149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec222e4c7d4cffbcbc4c28a2ea2a43e394f59ab93b6bc499419b0f55a9ca8b`  
		Last Modified: Tue, 26 Aug 2025 17:28:12 GMT  
		Size: 32.6 MB (32568796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408c578f5e14ceb4e5a7b13319701c6c281e37973f7494889b1280f61eb05340`  
		Last Modified: Tue, 26 Aug 2025 17:28:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4170619d52ed18a7f5de9becd42efc37fa96575accacbf45d5d65a0024535a06`  
		Last Modified: Tue, 26 Aug 2025 17:28:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:7fab7c99a859cfb463923072dbc983dd9c8eb8d3827d36a0821fc660bf1121ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ca4e04bf4b7a67784020d9d6efd14eef282e3674b9336cbb910d02da30c66e`

```dockerfile
```

-	Layers:
	-	`sha256:bc9be4c3e6d44f0abb8cea544a27de50388faf2dd24b7e30f5ab3cb27e38b7a8`  
		Last Modified: Tue, 26 Aug 2025 18:34:34 GMT  
		Size: 7.5 MB (7465148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ba2f84f1bca01a68ebb3e2fc5e7b33eb89b80bd1997713a81cf5f27f309126`  
		Last Modified: Tue, 26 Aug 2025 18:34:35 GMT  
		Size: 25.7 KB (25674 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be0662a7706a1e1f72e4be29514e13ee8a8af9d836d7cd6b65c65fb7dba40c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303465009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7d0f2d18b3f38638d044a0d74076fef41de4d1f986b1226fa479bffbc61757`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f78888ab9c57e95226c3244d90e801f0c238e605329f20de72d1f2676edd7`  
		Last Modified: Mon, 18 Aug 2025 19:02:08 GMT  
		Size: 156.1 MB (156081244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77414d354042d82c6e88bb0fb7123299d95f34013bc63dc9015c300d075ca84`  
		Last Modified: Mon, 18 Aug 2025 17:26:15 GMT  
		Size: 62.1 MB (62069068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880f134aff57aa7da0a1e88d934ea22212951ccb8028e2bfa2b26e2ea112718`  
		Last Modified: Mon, 18 Aug 2025 17:26:08 GMT  
		Size: 4.5 MB (4514158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02633ef455fe2d4aca91fc3ace5dcfad3651c2124338d746f6e2502c52b3280d`  
		Last Modified: Tue, 26 Aug 2025 17:27:16 GMT  
		Size: 32.5 MB (32457015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2805886651111caeb3109aa31a3b89de41770465d41c271628a64f40d892936`  
		Last Modified: Tue, 26 Aug 2025 17:27:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa45d9477fe4847059ea71e2e890618ea05d873e0a1833d1721cfd6b73b50ff7`  
		Last Modified: Tue, 26 Aug 2025 17:27:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:441da8a848d2e77e4dedc2a4fc5df849b4ddba43a3902b088d1934e7d97e0a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be1269574c1fa9919959d5dc983633ddfb24b65eaaa4413ee5d89f4d6a4153f`

```dockerfile
```

-	Layers:
	-	`sha256:1272bc56154549ca34a0147ce0a411414ee3f77ec2c2b19cab4ed82ad3aa8b1c`  
		Last Modified: Tue, 26 Aug 2025 18:34:42 GMT  
		Size: 7.5 MB (7470887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d023b85ed84e85fd80aa7e4f76c4eb520fca57d09ca4073661c06a254f02b8e`  
		Last Modified: Tue, 26 Aug 2025 18:34:43 GMT  
		Size: 25.8 KB (25798 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:843201064f31e2a571bb1c343b8ed190794a8a1f4e2c0eec9413f8262f5facee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315283868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a4404b8c09904cb7f8a57995276b575d71c0fc7b9424874c98198b59db47de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21178e342602edd12ca410499981adb42800eb941f19d77cad58cb797945aa34`  
		Last Modified: Wed, 13 Aug 2025 22:01:26 GMT  
		Size: 158.0 MB (157963474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c263420206d00133af94f1437dfd245a1a3a8f4cb1a9504d86890386c591d9f9`  
		Last Modified: Mon, 18 Aug 2025 16:57:12 GMT  
		Size: 67.3 MB (67318954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f5bdbc80af3ab1b08e7b107a1c862cb99020816e77fb3b10d880f5abc30658`  
		Last Modified: Mon, 18 Aug 2025 16:57:14 GMT  
		Size: 4.5 MB (4514204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593e6bbd79bca6655d0472b9b004d3561a273130c3e9d124a756b837f22041a4`  
		Last Modified: Tue, 26 Aug 2025 17:28:25 GMT  
		Size: 33.1 MB (33148082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7968104cfbe5dc68b5b5bb591916c93809d16529bc0221e50964db420ab90d9`  
		Last Modified: Tue, 26 Aug 2025 17:28:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5eb8b72c74697afb80848b0db16712bc9dae6bdf421317961a5daf8d2d30e5e`  
		Last Modified: Tue, 26 Aug 2025 17:28:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:cabc9e2c28de1a99bc111afe5f4dc53ed22bee81551df363ca59c3373007b589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16b735c44abdd088b08fd301f161b54e93057be6891ac49542df6e72b0a9610`

```dockerfile
```

-	Layers:
	-	`sha256:521327cdd085cc1116761d291b08fcf13eaa71cb7c508ea3df07c1a5e6c64381`  
		Last Modified: Tue, 26 Aug 2025 18:34:49 GMT  
		Size: 7.5 MB (7470340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76a39e9c5d6629fae653216285d91db69266691dec375800e97e28ae455c7a4`  
		Last Modified: Tue, 26 Aug 2025 18:34:50 GMT  
		Size: 25.7 KB (25713 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:cdbcf6e16ad6b44e9ad7fce3e993d133b4ff8d69752a75972baa1433ff9516ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292147793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8caf445428b112d1b34552e44bb5264024f6963bbb8173c6597af88e784ae9d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b459e3f0007c17bde237e108936432cad214c379e785f9e98e38f4ecd5eb115`  
		Last Modified: Wed, 13 Aug 2025 10:02:46 GMT  
		Size: 147.0 MB (147026949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b440b45e7ec283045c2fedd2fd1dd7a8dba5866c757f0efa397dc7a83bf238`  
		Last Modified: Tue, 19 Aug 2025 00:35:56 GMT  
		Size: 61.1 MB (61102791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc45fda15f79441d7ec88a560a7a9a431b3c44bfd89f60d50d34e790d85b9fe`  
		Last Modified: Tue, 19 Aug 2025 00:35:49 GMT  
		Size: 4.5 MB (4514188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aba2170680602f1017009b731e44fc7a8175c0ba5680746c71f89c9e41f3de`  
		Last Modified: Tue, 26 Aug 2025 17:30:35 GMT  
		Size: 32.4 MB (32352924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a745c28e137c2c07a7792ab547c1b945c53aa381cfa35f64f1cadb42253e7f2`  
		Last Modified: Tue, 26 Aug 2025 17:30:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5a6ea30fc21f2d27fa65c39734686764eec51d09b132435e4d47b0bc704d1`  
		Last Modified: Tue, 26 Aug 2025 17:30:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:02897c3dfb2188eededbdd5eb43919033a7747fafc2a6bb5fcfde0e386f41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4debef817b0ee4e718711894414cdb948e0c181a8d6ec71064fb71560448bba`

```dockerfile
```

-	Layers:
	-	`sha256:c7707b85ff78d8c4e66a1b86cb7c385c378306018f1d059496bf8789db388ab5`  
		Last Modified: Tue, 26 Aug 2025 18:34:56 GMT  
		Size: 7.5 MB (7456467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2dc63aabf5c79db83cab02ed243106acb04ea13f74b7313ac3a4cbe17f86895`  
		Last Modified: Tue, 26 Aug 2025 18:34:57 GMT  
		Size: 25.7 KB (25674 bytes)  
		MIME: application/vnd.in-toto+json
