## `clojure:temurin-8-tools-deps-1.12.0.1530-trixie`

```console
$ docker pull clojure@sha256:3657af6bf7731fd8262c8fd6a9541cc46df15fe1b7d38ffbd6a67b4a8977b68f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:750ef0b8f6850f047a1aed8841b431471fc1239efa7a09f10f0c301e2de37df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189222772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04c99e7e0361761989cda006714648ff51ab8461410f45e15fc739349eb0b8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33ec3b2cf56ad31185f65db380fc5018ff1fee91bd1a06a168aa95e9bb13dbf`  
		Last Modified: Wed, 21 May 2025 23:31:59 GMT  
		Size: 54.7 MB (54716171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37463d9a4e86dbc0ee4cd59586f8bb91d9c45b0b6d2a2c2a45b34d4faa12fefd`  
		Last Modified: Wed, 21 May 2025 23:32:02 GMT  
		Size: 85.3 MB (85259049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98d76fae2e764566deb297391bd6a09339ca13aaa7f80948772185580b9f20a`  
		Last Modified: Wed, 21 May 2025 23:32:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c989e08cb705ab6a9e71a71d257779f34d7041a928a7fb24f88ed05e60e45d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7454239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38039b2efff212965e1c25b27c2e966edbbc4c8320b8548525a7cde82701b9f2`

```dockerfile
```

-	Layers:
	-	`sha256:3fa23f6675953e2110872ae65c76c258feb72fe3f7aba3f3514df22c8d2bedaa`  
		Last Modified: Wed, 21 May 2025 23:32:01 GMT  
		Size: 7.4 MB (7440026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cd991c035cddfdfbeeed2c711d19046e351391d3e2cb33b5b74bf6644cdea3`  
		Last Modified: Wed, 21 May 2025 23:32:01 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3460c1546ff1c9b6bf0efed47b56e7c34d6db5c88b1bff58f30235f570fcdd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188624569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae97fad50db0f4208e859f74e49ce5dfa7fd0b22d605587702ae8ec5af40715f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0750f2222ba634ef6acb4ec68d0f6477201e94dc5d4d40912170cc287948efb0`  
		Last Modified: Thu, 22 May 2025 08:03:30 GMT  
		Size: 53.8 MB (53830506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e08267b6e2f571740dff57c9357fdc2dde64bb7c7612735e00782380b0790b7`  
		Last Modified: Thu, 22 May 2025 08:07:54 GMT  
		Size: 85.2 MB (85175126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eec74de994295e49ce241896a50bcf94ab10f566a21075ad278e76512ca0577`  
		Last Modified: Thu, 22 May 2025 08:07:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:46ea415b9eb7d7a4bdd528eef3682b0dadd1fe505dc984cf26ef8d36bf5de19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f488f19f919d50f81f66ee841594913222af0ced8db14c7512e0660ecc92e`

```dockerfile
```

-	Layers:
	-	`sha256:801afc6b636943bca6b6d941baa5068470c2764a2f5c02660c10dea9b33d8400`  
		Last Modified: Thu, 22 May 2025 08:07:52 GMT  
		Size: 7.4 MB (7447754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd4d09c5b7cacd52063c59bb161e0e2563e16811b9b894631af003a8b22cb90`  
		Last Modified: Thu, 22 May 2025 08:07:52 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5704032e65216da46cd2e57c16f4998250b446f0cb45ece577b58f7b951638d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195984221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b888fc7f8f1c9b01611f9bc445b34a056ed6638801f48d357c07c659fb5fd9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1676143d0c211519b773b6521adf180c811c58f3f9a5d2485e130a3de71661fa`  
		Last Modified: Tue, 13 May 2025 18:03:53 GMT  
		Size: 52.2 MB (52167968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6faed69ea0997395430df706271b547104fb40b48a4a4f64f227149f10b866`  
		Last Modified: Tue, 13 May 2025 18:17:39 GMT  
		Size: 90.7 MB (90743056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f374b639125f9ab855b32c0f9005d7824df010f3ed7efadf15eec5fd2a44bc6b`  
		Last Modified: Tue, 13 May 2025 18:17:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe75ca0158bf46456b0390c6d5cf2190b49e166a27509a1b0eda802ca27cdd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f953af4c18dca8dfc187087aa7900bdc6787d3413e85b141112f7c338a33384c`

```dockerfile
```

-	Layers:
	-	`sha256:f72a29f92366871f4678edef38e5952a8fcf7b313edb1e37d38ce99e037b5012`  
		Last Modified: Tue, 13 May 2025 18:17:37 GMT  
		Size: 7.4 MB (7395625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7f256a5e8b6c2110bfc3633d1640672bd83d38207b811713a38eb8a52e2dce`  
		Last Modified: Tue, 13 May 2025 18:17:36 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
