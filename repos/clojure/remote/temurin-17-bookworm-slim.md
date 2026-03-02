## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:91acccedfd897c1ebbea443bac18408a77711f9d1d35618539b44d3d1830e112
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
$ docker pull clojure@sha256:c30041776f1a8cc495255fcd8c9edcced458577650ab7cad202de65a2f08f61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243556989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ad8d34065b050a4ba1b0feea972c528d78229f99be1f90fadf53e81813c920`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:46:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:46 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:46 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:00 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe5d7d9b5e112612e6c79a0dbc11faba68beb3863640b92c1c873abdbd7fc5b`  
		Last Modified: Mon, 02 Mar 2026 19:47:35 GMT  
		Size: 145.6 MB (145628732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2025119ce3e6876e3cde1a0942ed37576b038b52b7a132bb46bd8b3de06a44be`  
		Last Modified: Mon, 02 Mar 2026 19:47:29 GMT  
		Size: 69.7 MB (69690934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad472cddc285b4bfc3ba3ad162be397313ca36248d1e2be7358adbe11e75441`  
		Last Modified: Mon, 02 Mar 2026 19:47:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0599460c95bb0ca3b3b63e793de19fb8d4d7292231bf4a8d72c71723fcc491ee`  
		Last Modified: Mon, 02 Mar 2026 19:47:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69a11b83c2c7a2a8fcb5c5ddde0fa23f118dc2d27ca769fafe18f02cfb00518f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e41ec301134e1b8ccbbfe5ae0d5c3fcd7041640126becb2c8889d1c35491ae`

```dockerfile
```

-	Layers:
	-	`sha256:e5b2a9db58491b64440b48338e5bfb39e677bc2eaa5736b5bb8d3546abf74365`  
		Last Modified: Mon, 02 Mar 2026 19:47:17 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b26b6f199f975a57fe36eb9bb84e9cefe09ce333d5a2289fd079ab37aa52ad7e`  
		Last Modified: Mon, 02 Mar 2026 19:47:17 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75499d840b160a8082f3fb2e94966f244137ca75e8dbfd853f5b5003f216aa0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242241255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd91345609323cf7ba0baca2b66b6e208dc1e4ff304794b5634c65d3f0fd33a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:33 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:33 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:48 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4174ed6e1c44c33dc821d3943acb0e3cfa1ef82c634e5eca32294cda36ead787`  
		Last Modified: Mon, 02 Mar 2026 19:47:10 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ab5e9e3cf2645c63c1fbd36f00024c1b4c05afa4c6c04abf8e8833d0e87205`  
		Last Modified: Mon, 02 Mar 2026 19:47:09 GMT  
		Size: 69.7 MB (69687934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e708a2e8cc67087d455c2fc8b684792cb0571dbaeebfff306f70a5f0ee7e1`  
		Last Modified: Mon, 02 Mar 2026 19:47:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb25bf534c2373edc1ec4192eed3afd3ccd993d603cc5bb6630a97575ba3962e`  
		Last Modified: Mon, 02 Mar 2026 19:47:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9772e5bcad7390354c69889cd421ad22c8ffcbc140a8803e794ca0c43a785d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032f7cd3270c0f099b866a6dba661f0421fb1af7eb9f3c7f5d5c31b37e0237d1`

```dockerfile
```

-	Layers:
	-	`sha256:36c49a3a17707696f203deaf0ab817b110b46ef3536add8f211f075f6975da50`  
		Last Modified: Mon, 02 Mar 2026 19:47:06 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b65cfc942388bcb3d2d4a5d451411afcabf223bf53a3f99d8d14b1b4f1d9f95`  
		Last Modified: Mon, 02 Mar 2026 19:47:06 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2c0eaed96ea7cc04db12ae43c491a35508c29675fb320b393c041ec4ff39c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253045503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67800c5d366e1cbef996457a123ca2aabd571e70261f642272b6e32250221e37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:56:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:56:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:56:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:56:20 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:56:23 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:57:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:57:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:57:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:57:08 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:57:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec74c10696e307ca8c4fff49f18ea11597d31a14db5de0982a3da9fa45d3e8`  
		Last Modified: Mon, 02 Mar 2026 19:57:51 GMT  
		Size: 145.4 MB (145438251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69ca5c44878ccb6e6bf54169964efd243d8564146a72047eb263fdd427db99c`  
		Last Modified: Mon, 02 Mar 2026 19:57:50 GMT  
		Size: 75.5 MB (75527876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df8acd87f5c65ad65f90278f816082dda2045293394e1e518e26ce05eeff45d`  
		Last Modified: Mon, 02 Mar 2026 19:57:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870a55f572cc1179c24246d09ef3fea749f971da8bf7491b4ee65d17b399be12`  
		Last Modified: Mon, 02 Mar 2026 19:57:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb3b30f5e2522bb33afd5a7b1dfb54438ec038270a45002225af52b1bff3c02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29323abfb324a8c29fdec34570d41d637372cc0e69053fcb0cee8170d2b97d93`

```dockerfile
```

-	Layers:
	-	`sha256:b2490631dbb871c4221640099d6987a984099f8914111a9707c1272148599d6c`  
		Last Modified: Mon, 02 Mar 2026 19:57:46 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1239cb5ad6b785668848478b251ae23a4fe6b537b64cbc2bcc9fc25e8166a69`  
		Last Modified: Mon, 02 Mar 2026 19:57:46 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f3d0f0452cf30d866672824b96948b8597cdc7443b8b441e2b12655eacb92409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231023346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26187961380e7329f56b9c0ef5268511ac13f0cbb0c21d316a0455f8e0941e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:46:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:10 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:10 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:24 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a941371674484988329173b2d1a9e85c7244c1eeb6ac99f63e86c9018c0b3416`  
		Last Modified: Mon, 02 Mar 2026 19:46:55 GMT  
		Size: 135.6 MB (135627062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778c70aeabfb1cd85d21fbc235dea6c92588517669c9820a82209aa01490c1e1`  
		Last Modified: Mon, 02 Mar 2026 19:46:54 GMT  
		Size: 68.5 MB (68503716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75842850f26cea7c1a1edecd49c276002da12f0c05857a646baf294f25000f`  
		Last Modified: Mon, 02 Mar 2026 19:46:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6478af050f9f49b94c4036ac5507e0c0449356bb777309de6376232bc3ea7b61`  
		Last Modified: Mon, 02 Mar 2026 19:46:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7376bf9292ffac179cef87cb9fc8c28f56644a3fe428e9509a29ef0f88f12cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b913feccddba28f67bee9abdd09121f342aeafca7b9e5f606e4b90f44766b0e`

```dockerfile
```

-	Layers:
	-	`sha256:7e9fcbcb7bd0f1408ebcc8306b9fd3d20d439bede852f62c0e20e15160412cde`  
		Last Modified: Mon, 02 Mar 2026 19:46:52 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f3be19134984b21b226264ee51c9e801e7c740948f0f8155fe29a7c4cfa86c`  
		Last Modified: Mon, 02 Mar 2026 19:46:51 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
