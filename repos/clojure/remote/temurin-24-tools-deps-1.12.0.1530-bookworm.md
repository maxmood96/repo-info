## `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:6b77b57520f757d2a86623f475c246f703700817237e7459222ebf5a1fe00af8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:321c216d5bc3045e887af7042d9eeb6f40abea42ff9b931c7dd5981b37651964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219435897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab186b62e1f5cabf06936a375c59e2ded4514eee0b17b3c60c331209513cfb3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4c36b67d1e87fdfbd0a543b44f2d18a820f9d745a3020517f50f7411c1d339`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 90.0 MB (89951978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004469d78de90c6c6cf80934baab296babccd747813a4e69c63780209e4b4bce`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 81.0 MB (80991682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124974ae99275abc7f293c99469d2a07f300bb7a76bed21dfbc2b17bcae1984e`  
		Last Modified: Mon, 28 Apr 2025 22:08:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9efd428bca3e124ab4d024d464cb1aa06aa196e13f9d10405477841b543ebe`  
		Last Modified: Mon, 28 Apr 2025 22:08:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f86821766fb9e7dc5ab563ab461bb8f3c3cdb254fa0e53ff46ace9a21f8261ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d252796708e13cec2882bef8ead256666d06343c2631ca783c32609d767d64d9`

```dockerfile
```

-	Layers:
	-	`sha256:d27cc174e963be3d356fe399ef7c4254eeecaf960643d04fced0e3b355dcb413`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 7.1 MB (7123806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457b7ef4f18d2fa18fa3f6873cb797ec6e732f71bf1ad1fc277255123e3992b5`  
		Last Modified: Mon, 28 Apr 2025 22:08:10 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:515d21ba904180a8bc0bbe856d6ca9d1715fb0ce4420103447df65b538fa0a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218263772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce830c1a4927567ff87f0c73a4e1c3b6ef0643b37447c90fedeb348ba52a0892`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d29a9fc32a83e7866e7172e5148e804d7fa6b5e264bedd1edcbb3907d41e8`  
		Last Modified: Wed, 30 Apr 2025 01:49:38 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceec8f5e8b270bccbb1e7666f3c2abf66341fdddb2d080897610d749047b6afa`  
		Last Modified: Wed, 30 Apr 2025 01:49:38 GMT  
		Size: 80.8 MB (80843855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f1f42350d9b5f1ccbbd8b67ad5421bf6b535226ea54a3cac188a895fd67119`  
		Last Modified: Wed, 30 Apr 2025 01:49:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d097471bb254acff10d2de2adc6a2b59e987200d20b70444a753ff93a5c256c`  
		Last Modified: Wed, 30 Apr 2025 01:49:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5b43e1d46c3518ddf31ac375d8bc55820d50215354ec32dfccdacb8cf2fbcfe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276c09983d2785f5790040f361cae98823af05b1fa9e4fc00e06d94608a6f2ca`

```dockerfile
```

-	Layers:
	-	`sha256:d5476bdb161f4ca2f51dcdef2a784fa806c1a6cfd81e1f2d41888b2b6d5fc850`  
		Last Modified: Wed, 30 Apr 2025 01:49:36 GMT  
		Size: 7.1 MB (7129590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e945e65e4aff960b1560e67c06f4d6acc396d391589ab6e218f4651d1c184ecb`  
		Last Modified: Wed, 30 Apr 2025 01:49:35 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json
