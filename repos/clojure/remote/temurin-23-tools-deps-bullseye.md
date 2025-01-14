## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:659b5b029121905e08d8501cd999f307b994daaa41e064ee2afb647d2ff6b8f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:249de46bca9e53a40053d74271d79f966c899298ee58fee738b030ea0d564a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288214295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849ecdce67221a9e996e18ff35e76d6a2c91f6890adfca25209bc1e1c34b5704`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f715356689809cfa006ecca92880319feba0102bde94c101cb5dc31f013df9`  
		Last Modified: Tue, 14 Jan 2025 02:45:21 GMT  
		Size: 165.3 MB (165295091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35292e87fe6b72f41b521be38aba2832d3b97b2b2c96c5aacd34657bb9de56a`  
		Last Modified: Tue, 14 Jan 2025 02:45:19 GMT  
		Size: 69.2 MB (69179003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7f7098a71c257b3da781d7df96bc927e65939a829f5eebc0fea6cea109db7`  
		Last Modified: Tue, 14 Jan 2025 02:45:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f378be04143f7ef7bfbfc44ab3056ead3225e42ef7e5182604c2c2567ca39fb8`  
		Last Modified: Tue, 14 Jan 2025 02:45:19 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:59cec27e74a62073f08d1d504785d4ce04dd3da1bc34598231240c218a3b3375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09aa327915bbc9b9a71c1706108b94f9d10812475cce6d629e8b0bb3d96ee1ff`

```dockerfile
```

-	Layers:
	-	`sha256:6f18641359d91371bb4db16b8e7a324b4dbbd974ddd569e84f144321eb82864b`  
		Last Modified: Tue, 14 Jan 2025 02:45:19 GMT  
		Size: 7.2 MB (7209562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113a71b1fd99368b142577f7aaa3c1ac2960e0f944afe83fd61320f7ea19a030`  
		Last Modified: Tue, 14 Jan 2025 02:45:19 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9325c808f279fab8e0fc12700bf93e04b0b5d5714b0cef6b2ccc38a069a0e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284832956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de8f3615aa743a9478ba1cae62c0b267832ff3956a78f2c4dfa250f96f6ea4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6695db2a9af9c621e2afd751a22f972795b62d6695e9f4d372982636e107ce9`  
		Last Modified: Wed, 25 Dec 2024 07:38:55 GMT  
		Size: 163.3 MB (163281797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dd2c383d7ef7000b8c926e035df3b7533324603e76960f5d756f1fa930a66e`  
		Last Modified: Tue, 07 Jan 2025 03:37:50 GMT  
		Size: 69.3 MB (69304419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9265ef8ef3a04d7e024607bc89585190553562f6db7ac2600642cddcfa05c9`  
		Last Modified: Tue, 07 Jan 2025 03:37:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc61c3d807ca54763426d319e45caed0bb227d75afd3bcae11683eb0cae6f201`  
		Last Modified: Tue, 07 Jan 2025 03:37:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d1488704e0a6665b7263188a3cd3ba310ccd3e948e74c0a985accb3ad2b061bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0dc379243b62fdbe5f3a515408a338867b06b53df6369ba50fa6443b3d91041`

```dockerfile
```

-	Layers:
	-	`sha256:a4f17f747d269950da61e550f94fc493b23c7aebca583810bc4bf37941ca343d`  
		Last Modified: Tue, 07 Jan 2025 03:37:49 GMT  
		Size: 7.2 MB (7214040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d5dd624580ed291408e3e62e573148001fef6fb8666e66d78deea96a754fa2`  
		Last Modified: Tue, 07 Jan 2025 03:37:48 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
