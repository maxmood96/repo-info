## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:1e2c9b95ee9c7e18249975eface5de5516aa17f3f6591cf8f1267b2ef1d0776e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:78b9b2232a2ac2cf336c742346b0a87099c466cdc19f332e659f3d3e6b889798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234641493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78409646364f431f7e11d1e4d469a8e3b71e6512ebcd4b3c479c46f7dccacdd2`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e86e61ce922815b96dd61d5008d9a35369e96a1e3d5c9652b7bceccbf2f0582`  
		Last Modified: Tue, 25 Feb 2025 02:32:25 GMT  
		Size: 145.6 MB (145598937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9615d3b26a5fe2f6800520db06d6de7ace81769797058adce13ae8ab210b67`  
		Last Modified: Tue, 25 Feb 2025 02:32:24 GMT  
		Size: 58.8 MB (58787980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9f042aede2abac7cb25a3b7abe840b31520037aedfe04192cabe56d8d2e285`  
		Last Modified: Tue, 25 Feb 2025 02:32:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc9861999e5df77bde45ea562fbda2ac4b078f957511a690803b756f876a2b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfbf889a137bfd2de5154e76c28c50133355223d274d57c24470354ec81b15`

```dockerfile
```

-	Layers:
	-	`sha256:99a7fe1eff73508093f614feaccc568c1071ef734a685566c3c2f5fe1190c975`  
		Last Modified: Tue, 25 Feb 2025 02:32:23 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d9a11fa3e6dce4be5c21e2f9970e204debe5b47e3036e1868d0c99247b8069`  
		Last Modified: Tue, 25 Feb 2025 02:32:23 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66a43044cfa676c2e84a642318c17e1712b704c727f0915f774d94e994474083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230042363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7afd78d2e7cb3db7f9bc78f4f4654368729cf407eeb7c35decd5084cffdcb46`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9636195f78efd3d4aece88ef3898ffd776ba2f988cbb2764f04e0a2f6a19e3fe`  
		Last Modified: Tue, 25 Feb 2025 06:10:07 GMT  
		Size: 142.4 MB (142385384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9c24ea17c6388eee9b0b6bce7b2c49f78b8e85592470ca3442066078ce0ef`  
		Last Modified: Tue, 25 Feb 2025 11:01:43 GMT  
		Size: 58.9 MB (58910345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c923748b26707579fd82203d329777148c4afdca6433a0b8ad4988bcd82a9ddf`  
		Last Modified: Tue, 25 Feb 2025 11:01:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd85268f4719d33d2f3ca4386c0071ea151fa18b703c9723b74ce39f090c9f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5c1e4263f2eca4b3c6ff2abc41eac9083b6123cb138790f783603d1af72b8d`

```dockerfile
```

-	Layers:
	-	`sha256:f868acbc085a96ae7b9a1c179beaa89425bac7b77401cda598b4a73f556dc786`  
		Last Modified: Tue, 25 Feb 2025 11:01:42 GMT  
		Size: 5.1 MB (5143558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45a11c66e6963a431d98cddba8add7805a041903a7da2b58a12aa5046ed48dd`  
		Last Modified: Tue, 25 Feb 2025 11:01:41 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
