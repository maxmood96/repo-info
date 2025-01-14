## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:d7c35f9da603f19ff601c0742c3fda3c931a7f1142ab850b1275bd473f87b19c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a8eb81acdbe107f5cffc86eecdb3cc7146c23b93b7ff75b2ceada1693c5f9e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275059932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae120c8efd3dd95e2614e99ebf9e029cd1d2865c39b231423e740168dfb6bd9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d096d5a0db988ade99640ca4ffd661862ba3b5d808f57912dea49f8736ade427`  
		Last Modified: Tue, 14 Jan 2025 02:44:01 GMT  
		Size: 145.6 MB (145601458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac6a9e8a919d308685e02f30b4a5b1fda5ed6dba755155bc3c0125860a92a2`  
		Last Modified: Tue, 14 Jan 2025 02:44:00 GMT  
		Size: 81.0 MB (80977867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db16498cc54748d2d54b8bf9e36c5a24af4705bec98654597b19e631ea629c`  
		Last Modified: Tue, 14 Jan 2025 02:43:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9412a47c0fa66f1b841f6fb05285ad7af425dfa501a8cdaaf52e4872b2917778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57081a0fbfc4f80289b7544a56399e38e70768693e27df9c4f77617fb8ee359`

```dockerfile
```

-	Layers:
	-	`sha256:5ed65cd4fc6e524649336c8d095e69e7d0f39bf80cc7c0c453277d58b9c73c41`  
		Last Modified: Tue, 14 Jan 2025 02:44:02 GMT  
		Size: 7.2 MB (7191219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16269435e369961ae4348c1dbab4879f0e0526a369db1afe3f6f2743af2448f0`  
		Last Modified: Tue, 14 Jan 2025 02:43:59 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c3e0fe426c99b10c068211e126e15506b45924acbc49c31f7171e4804a5198a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271339395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b372e279907ce7aeef15a8e06bc64471d8b52799495fd488ecfa1a2b9fe82a1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b316b6da7602d7d947fb3a1a3a4cb0c5f81ac14644e8b0690e4182e479910866`  
		Last Modified: Wed, 25 Dec 2024 07:18:00 GMT  
		Size: 142.4 MB (142389012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4330f2c29a7ca4acbf5f07d0001d5267f98dfbe9cf4541b6b0dd184b1215e97`  
		Last Modified: Tue, 07 Jan 2025 03:22:21 GMT  
		Size: 80.6 MB (80624255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bdbc5e4bce5daece28078ae44c38703a6a73cd5c33af3157ccf661197306e0`  
		Last Modified: Tue, 07 Jan 2025 03:22:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4fbed273e00cf256994e3a1b9b33f8a47c5130f1c7e92f61ecb6dae6547061ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e565e79ddb8ceb50aa77569f45c2941f27dd25861f716344daa5231756fbde`

```dockerfile
```

-	Layers:
	-	`sha256:4e4ace47bd1b3ba1e5e409c6b416ab773d6accbecc5d372a7e1a25b192f4b8f9`  
		Last Modified: Tue, 07 Jan 2025 03:22:19 GMT  
		Size: 7.2 MB (7197600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd7035e91f39ae6e1a968966b667a930ac1c211d479c8158c789ec2afedbd128`  
		Last Modified: Tue, 07 Jan 2025 03:22:19 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
