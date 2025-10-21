## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:aed04503ba099aa4a8e42db5bade8213fea25c7ebebf4d4f9c466ba719d825c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2791f7e00e3bfa74292aa9fe7a5f1637f326fd3e906514415dedd3721dcfefc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a340acfcaa11ff514f8c7416cad39be2c0ccc24e056efd9ecc2bf13f2679d8b2`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa80d3b70a95fe20254707031e4cca1ecddcd0e6a64343bedb1fddbebfd2be7`  
		Last Modified: Tue, 21 Oct 2025 02:19:50 GMT  
		Size: 54.7 MB (54731346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84214a1b33e326fe612f64cdba784a44d380ee5838e4add26590703430eedbe`  
		Last Modified: Tue, 21 Oct 2025 02:19:52 GMT  
		Size: 85.5 MB (85542569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66980d067ea5d50ab208788495f74f12c0b55b4f098d139d22bbfd60ad9f6ef3`  
		Last Modified: Tue, 21 Oct 2025 02:19:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3f046665571ad26bbed0366ee28dcfe68997f47803820b45701dfb3be3be6ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a62f47c63976bf8d71bdab94da0868e42ee06cbfadbedaad1f7d5b936acfdf`

```dockerfile
```

-	Layers:
	-	`sha256:03bd8fca66ae804abdf2f50aa6c418d95002ce8c46871aa15e8d8976404c4f29`  
		Last Modified: Tue, 21 Oct 2025 09:47:58 GMT  
		Size: 7.6 MB (7588509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa69c78a37d7211f2e9c11811eee4186b6128ac051cc1ea4a5f712f41348d0c`  
		Last Modified: Tue, 21 Oct 2025 09:47:59 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0ac48b028977942d579878e0f3efe9c09193d5b69e8c9ee4bbdd5e414132f9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188848999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d0ba08e5dbd707e226860e3a02e3a3585abff5ca3887b7c5d7f73213f0341f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc45b158196b34c8aa2a8073eda23ad1fa5e528b37a3a9604d6611c357cb29da`  
		Last Modified: Tue, 21 Oct 2025 02:25:34 GMT  
		Size: 53.8 MB (53835610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e18f29fe9de17bfed0f1ba52609c2a65e3a2e11c86c97aae421884b3fc2016`  
		Last Modified: Tue, 21 Oct 2025 02:25:36 GMT  
		Size: 85.4 MB (85363001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e337f6c5368675a7518ffa00d6f811667123f98c10d87518197337b9a5b262`  
		Last Modified: Tue, 21 Oct 2025 02:25:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5d0aeb094c45e2012866938086a3714decc6b60712a8b50994565b53916977a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcc9d76885b0d76c4c2afadeb81b371592fc838ae791a081f3f770cca897fd1`

```dockerfile
```

-	Layers:
	-	`sha256:5ddc45eeeb96dbec00eae98498976d08680f5bbc87707492234e9e2604096a49`  
		Last Modified: Tue, 21 Oct 2025 09:48:05 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d50853491e20228f0e0b7e247e9eb3c33ad1b57549faec57a7440cce1bb743`  
		Last Modified: Tue, 21 Oct 2025 09:48:06 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d78e73a24ad5b252dd24bb999e80de24c6ef39dcaf18f5d2c823e5873fb08adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196224552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec46cb8776949cf290b777e1ba1b94977aa0e1f56daf1f8041c87e3663e3255f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
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
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdbe0b60fe16dbc11b505a333d9eca1bab3f0320dc1c61278729bec87a034af`  
		Last Modified: Tue, 21 Oct 2025 15:23:23 GMT  
		Size: 52.2 MB (52165398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135d62fabcf368ee8f6ad1c6330f38937978b0e3ae8cd36ea6a5125be58e1df`  
		Last Modified: Tue, 21 Oct 2025 15:30:07 GMT  
		Size: 90.9 MB (90949035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379db0b40c455fe6e8553bd3c86584973d8e41be1668249d1defa28bed760c6f`  
		Last Modified: Tue, 21 Oct 2025 15:29:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5bba7dd7d34a38bc32155f4bde511f60d25d602197ed23c94d4b4758640b78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97915d177720fcdc765d21f9d50c0e1078dacb00b2f0b1faec19465dede5906e`

```dockerfile
```

-	Layers:
	-	`sha256:5e6c9fed0e5bc42128691a47a41a892c8150d917f71db99dd13d6fa7952b231f`  
		Last Modified: Tue, 21 Oct 2025 18:43:02 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5dace573a3d66e918c9b9cc0e686c240660138ba876c3c59726167e22901e9`  
		Last Modified: Tue, 21 Oct 2025 18:43:03 GMT  
		Size: 14.3 KB (14260 bytes)  
		MIME: application/vnd.in-toto+json
