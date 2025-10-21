## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:2342f2d4ecc5fa7b579e08fe101c00ae5b34fd10ea4543be224140fbc7c5b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:79b8a3abe2a51053bfa69bedd6762e3caa153736cb06d5fa797fe0287af52c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144141288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c441b7917cb0928850bb866f545297c425c62ddddfaf205b885bac988c9eb7`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
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
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb08fc87192ce9a4c75c6a41c29cec99d468c922742b3cc5bda17b7274a0bef6`  
		Last Modified: Tue, 21 Oct 2025 02:19:52 GMT  
		Size: 54.7 MB (54731351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96d6c9cf19390e96d638282bb0ac7f41c3826c16d311c086b1dff75ae899d5e`  
		Last Modified: Tue, 21 Oct 2025 02:19:50 GMT  
		Size: 59.2 MB (59150927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df1d8408fffeaa49722cf7d1937cf72afcdabfaf40caf5dda3cd7439b0421c3`  
		Last Modified: Tue, 21 Oct 2025 02:19:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b9bdecb402c29e4364c878912764ab472366dd68651d298fd76423454016737d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78179200a4bcc3700bbde4ff59dc250b2135cf8963b834fc2d6360700d945555`

```dockerfile
```

-	Layers:
	-	`sha256:adb7b7293a7457d7683d8bff2bf049f134aa6ed56fd06c87a680bac00d820763`  
		Last Modified: Tue, 21 Oct 2025 09:46:29 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f75b6bc0f28be6a0a451293ac12dd509005aca1c931d53fd80d0ff534338d9c`  
		Last Modified: Tue, 21 Oct 2025 09:46:30 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:13f2e15db97143484cb06d940ac97f535828d8c0b8eeaaab8998cfd06c8b1aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141871555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1d2155efc607cc4dbaebf24672682c4247c397a9bc83b95f85225a2448ce54`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
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
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c18316e75689ee5e86e6d41a110e240ca554e852ca6e6f1f6dc9b8cff5910af`  
		Last Modified: Tue, 21 Oct 2025 02:25:23 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e793a8009af9207960d6ba82b380791b9f9a2681b58a0f03ebc00baa7f76ed`  
		Last Modified: Tue, 21 Oct 2025 02:25:23 GMT  
		Size: 59.3 MB (59286903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d6d65bbecc246e6607455360acdf116571b64336c8fb2a1e7f7089cee691a`  
		Last Modified: Tue, 21 Oct 2025 02:25:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b9b14198d92829b204474f3156ca747056e301edf7087803a1de36c7bbacf967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7db812095c03e9e50dba4b43c7dd1257dcc86454e06cb49290683401bf79cb`

```dockerfile
```

-	Layers:
	-	`sha256:2479c3b6a59fb75f1128144694207da8890a7c75cd85f383a15ab51e9d47828e`  
		Last Modified: Tue, 21 Oct 2025 09:46:37 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92edd24fb8cc620e949365a28fb2621bc032d0a7f1654773a32b8c333c6b9877`  
		Last Modified: Tue, 21 Oct 2025 09:46:37 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
