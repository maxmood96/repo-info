## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:5d9390e15d27f177a75e896053b8649fc9d082685f890f10b2b93e78168fcaa6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:17a44a097f296f8bf3e11db7d2a53dd97277462382af10ac2991e18d2967d176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243343271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51a06b5fa093ddceda6f0bf7eac32d165e7555cac1eff9a276a9542d405b5f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ddbb4804d79c311dba99b3e33e2c34a68afa7c1deb824ce5ebfbaaaccaf21`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 145.6 MB (145598771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5497a2173c6f0c7547f6ee644b8d97ed1da05e58114db6f93884487892e802`  
		Last Modified: Fri, 31 Jan 2025 02:17:46 GMT  
		Size: 69.5 MB (69531437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e3af3bcd2046a996691e8e5af4d97f4a08fbc5801b6e73d1ed0f6d64f86461`  
		Last Modified: Fri, 31 Jan 2025 02:17:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8368181df6999bd692d213a3d68ae721f59e8a79bd8d2cd49fc60bcc347ef47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b426bbae521430c9d68df23ed83afe7be60cdb04d517050487fcb650f6caf22`

```dockerfile
```

-	Layers:
	-	`sha256:d472ff32372fccbf4a2ce533f7f6eb43c63943d3fcf13f11c269b1d80f62abd5`  
		Last Modified: Fri, 31 Jan 2025 02:17:43 GMT  
		Size: 4.9 MB (4932708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d77003eb6233a3626ebf41eda3d2d31b26d9b509371f2942d2624b30d400cb6`  
		Last Modified: Fri, 31 Jan 2025 02:17:43 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59499aaf9ac42d48533372f4f42010e52630d6d1edd6e9c59c0dd7c651fd91eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239808949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6579010991a009a5e992d42233be97a8dbcdbccf9c86c182d456444e327c87`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9060b028d06a8fb22c11eb150c07167cbc0d14bcb2ea774f5d7146748ed43f`  
		Last Modified: Fri, 31 Jan 2025 05:02:00 GMT  
		Size: 142.4 MB (142385501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bce7986d1c8a409734dfbb6960948c461f101b74dace29dd180c9b7985d258a`  
		Last Modified: Fri, 31 Jan 2025 05:06:28 GMT  
		Size: 69.4 MB (69381773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff1ebce4ef9db6d767f57999a2ecc75b9204b5fb50efdfcf6bdae9d01a61b8d`  
		Last Modified: Fri, 31 Jan 2025 05:06:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2eb5f9b6357f7bd1b07f391dc8998ada61128437c18c6abcddb11be141107b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cf6bbf7c6c256584f273aa3c6af79d43ab3e4b93dc88a396665662d3363953`

```dockerfile
```

-	Layers:
	-	`sha256:9b729db41ce302fd05470ab4e07b7ce0a2aec96dde90740bcc259bf6f26cb461`  
		Last Modified: Fri, 31 Jan 2025 05:06:26 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279fb210626d7ee5f01d80a11e9793faa0efa7fa8356e2aa28ec06c9c04e58de`  
		Last Modified: Fri, 31 Jan 2025 05:06:25 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
