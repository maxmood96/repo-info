## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:4eb82e778b76f341650a6d362ff13302edd65a5fc938d6c2d041cab756b17638
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d0aed1f99553b98a89aeb10c57fe8a1f3aabd95a5ac9eec69033dd4fae9daad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144141964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e7a8381c6df805d9422c89feae48723fb7c7c14a2f7a320c8f84ef0bffbb91`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047783f1244fa23155527f35e3af3b9fc465cc9b4e9653c18b57cae822c7c570`  
		Last Modified: Thu, 09 Oct 2025 22:26:08 GMT  
		Size: 54.7 MB (54731351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3536eaaefedb2d2c3520f1694c0af7fddbe4b4d6b640b15ca97922fb5693b7`  
		Last Modified: Thu, 09 Oct 2025 22:26:27 GMT  
		Size: 59.2 MB (59151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972f9dedd18545c6bc28ee28433509885150f3fc3661d9972af76df842c747d`  
		Last Modified: Thu, 09 Oct 2025 22:26:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:030fa5a05be38ff0bbd847ffbcfb9733359b68c9163e042935e4e0503a1d1292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937b10cd1cfe7cc050df64e2172a129d14e59ff08c9472bbcb926529aa5bd48f`

```dockerfile
```

-	Layers:
	-	`sha256:356746bd0ff1ad56f83d7bf805bd7d2ccad752e1722f13e5770333788fa39358`  
		Last Modified: Fri, 10 Oct 2025 06:50:24 GMT  
		Size: 5.4 MB (5431301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7a93266fba847ea038ba6e303eac54cb82761d9d4e43319e56bef47891a01f`  
		Last Modified: Fri, 10 Oct 2025 06:50:25 GMT  
		Size: 13.5 KB (13491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e63260d1f5c82016ada0c327158aa469cc6e5463baeebfe87a9f759f23d5d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141872085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df0546a7dee502423bfb0875a0464aa31c27ec3a359cf139796b3ff822a9e10`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3731f051d3e78d40edd7d1958319a23436a0950be73857b6bf9e90623f4cafe2`  
		Last Modified: Thu, 09 Oct 2025 22:26:31 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f3fbc1eda46206d9bfed77f1059f348ef8ed92946be36a7c6f356e5dbfab66`  
		Last Modified: Thu, 09 Oct 2025 22:26:33 GMT  
		Size: 59.3 MB (59287408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641b2a359dfb3b0366da1b78b13c5f936380fa72597a75c221697e3285106a57`  
		Last Modified: Thu, 09 Oct 2025 22:26:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f6500bbfa09f0b0a3f32779c00ec8b058329c3ff51386eb024c3aad64bd2fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4134672e9c8943c962eeecbc6de0b0c252d199d77d3a63dffa51a4aa6d649208`

```dockerfile
```

-	Layers:
	-	`sha256:24cb371855cdabd9253e530cb73c982ce54c14bed1f29ffecbc63eaa3a5f0e7d`  
		Last Modified: Fri, 10 Oct 2025 06:50:32 GMT  
		Size: 5.4 MB (5437731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31435a70187ade3ecdc8e58ff8ae15c8b8ac7ce6bf36b4d69054d797cc6127c7`  
		Last Modified: Fri, 10 Oct 2025 06:50:33 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
