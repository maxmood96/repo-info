## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:1f09e7facf1ac4df4c98d39166991bbd1d29f9f79f1345e63e636af34465e689
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ca3851b7a8a9f84af417846be2c20c5abe58b543ea46782ae71959c33129e08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257679463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881fbe508fc5eac62372cf692e54290360133cf847b8e806bd1dea1c61c35ed4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e399ec2b2438646461a97708a384df1216e09e88a034a561a7d79f74accae8`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 145.6 MB (145550069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ff67b3a5df0db15f98cd1b34c0d31b1347d6ee0b752aa21e1f04d2544c6e96`  
		Last Modified: Fri, 23 Aug 2024 20:02:22 GMT  
		Size: 52.6 MB (52646650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6e6c83ea2453c1069412ab599088561e3bbb93f4b6c508f1e0c911654638ff`  
		Last Modified: Fri, 23 Aug 2024 20:02:21 GMT  
		Size: 4.4 MB (4398037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c9ebc895b00b18fc18f633bb9b71b54c6632ad061ec35162ede32bf22fe136c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aa9811b97c3cdc25fe00a144c8a5aec0f0e805e1b3728a062d8ff8f8a2d9b5`

```dockerfile
```

-	Layers:
	-	`sha256:6be81b7ce4ade624959e1914875cf1a164e101f778ef63504890a468add584f6`  
		Last Modified: Fri, 23 Aug 2024 20:02:21 GMT  
		Size: 6.5 MB (6455489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3d46fbcf921d71314b34ea542db153b488073b47049638d20ae4e883fb7582`  
		Last Modified: Fri, 23 Aug 2024 20:02:20 GMT  
		Size: 16.0 KB (16045 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bcee3be8a5328940e718370f6065e726f2ce8ee67b9dc513ae8676e78ce244da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253144105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c649432e1c941b03eb884190365106416decd55b9a5fde501c6e044f61bb98`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e8ebc81e83cb3ed4b3fd4fb1931a80994977bb615a00cddc5d409eff357c23`  
		Last Modified: Sat, 17 Aug 2024 06:03:04 GMT  
		Size: 142.4 MB (142354842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06eec782e92c5fa447d64a607f2ef3b3f626754d1c85c29aa4864f8caf416a3`  
		Last Modified: Sat, 17 Aug 2024 06:03:03 GMT  
		Size: 52.7 MB (52661272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1df698797409e1fb62111620eabfb9a3db95459b29ae2e3b14fe792bc6a7798`  
		Last Modified: Sat, 17 Aug 2024 06:03:02 GMT  
		Size: 4.4 MB (4398038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:77b9f0c302706b78c852e25e84cf1f0248193bc83d01d928c7cd7e86d1064acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6476882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d8cb5722281e849454f41f10737c2787659907a2c488f328477c9d93ee4069`

```dockerfile
```

-	Layers:
	-	`sha256:4c6bba9ee14e7715f960874c306e1ef15e019c6111a54d6f8666b6af2b23e202`  
		Last Modified: Fri, 23 Aug 2024 23:51:21 GMT  
		Size: 6.5 MB (6461143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f97a1dbaac4931dad5c9c0eb4d543295b799a2616b7fe5aee0ed85ce36f00e`  
		Last Modified: Fri, 23 Aug 2024 23:51:20 GMT  
		Size: 15.7 KB (15739 bytes)  
		MIME: application/vnd.in-toto+json
