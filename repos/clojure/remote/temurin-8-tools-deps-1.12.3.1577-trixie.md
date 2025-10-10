## `clojure:temurin-8-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:7c4bbc546750a3433f0948ac43f53f931a3badd43e86877afc44adace7d3498d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8cb3412d4ab265b7a75df65bdbc164d8a2d686d7b40648433ec756b64f60c325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192515124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2835fe1d6a45f85dc43cb5a0b2f7595b6ed5281afd3d58bdc53158ae28779ff8`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4cfefdad9ccb90cc381a730e38e0fa427ffcc843d5fe2d9a080950e3ea9f58`  
		Last Modified: Thu, 09 Oct 2025 22:26:44 GMT  
		Size: 54.7 MB (54731353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147c797feef08646793646463c5f13d5a3b9e381554f5fea5e1d194b1d805cf7`  
		Last Modified: Thu, 09 Oct 2025 22:26:45 GMT  
		Size: 88.5 MB (88498500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a303f2f72c1ba945da59a1a1cbbfadb3a779b82075a7d4bebf3f62dfe22833`  
		Last Modified: Thu, 09 Oct 2025 22:26:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ef1678095e128415ff4369484b4b0a0f04a408dfd648da6d1f3538c5caf1e2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d916543f6294b0fa11854056ab10e22f7251247c126bfcacb3de93f0dd8f2859`

```dockerfile
```

-	Layers:
	-	`sha256:9e3e2c1d7a6ab360aa38ded27fedf02330542010a82d9854e36a248e03a003d7`  
		Last Modified: Fri, 10 Oct 2025 06:52:48 GMT  
		Size: 7.6 MB (7588509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4493b92f7d510a508349af1975086ec9e90dbc52f2d4cbfdcbae9939d9b87f`  
		Last Modified: Fri, 10 Oct 2025 06:52:49 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f913e7bd6edf28adc084cb85cddff1f0107c28324851e8c0f2edb9d87cfafd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192175654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccd09d0f9e532716ef8679ca18143066ae595720b8e8ccc76e5ea2fc5e225f0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b5dde024c78cf2d2cf9e8deb373aacd155c310db0b45c68be08e91a9ac255`  
		Last Modified: Thu, 09 Oct 2025 22:27:16 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601a19f957b4dfa86a5f4dd6183749a2a9626bcf1ca76335afc019a18251c4d0`  
		Last Modified: Thu, 09 Oct 2025 22:27:21 GMT  
		Size: 88.7 MB (88690708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9a2b3ebf5df26e3200cc1d6ba399e7041153fd5b3de817292df44c6d5cb034`  
		Last Modified: Thu, 09 Oct 2025 22:27:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:80d1a656522dbb84771e7a1c5a2fba6294c8c0ccac64015a42eb55e27ec52b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545b635d5a2707313e54fde7a52004ac4c125475c022b6927a674db5508d270b`

```dockerfile
```

-	Layers:
	-	`sha256:03cb9a8729cc26d3a4bfdc0037e4b82b750d2959c86d7209e804b71cac418c31`  
		Last Modified: Fri, 10 Oct 2025 06:52:54 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186fe16411d89b67cbbfa65be012be1e0f8ca6c5e0e61bfdb385b8dbbec31ade`  
		Last Modified: Fri, 10 Oct 2025 06:52:55 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:74ce31eed6a2635caeabc2910f7f0c1fd80716776824aca129ed0014a8c5216f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199426985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0366366e3a17132561e81684e964fa603a1d49869180761736936d992c61d37c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc3f1eebf7bf9dd53e932366fac151524ad2e096efaf95dbc9c6f9b71a05479`  
		Last Modified: Fri, 10 Oct 2025 04:46:14 GMT  
		Size: 52.2 MB (52165419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7e789d5ada28f2debbc3edc28b5d70a23ecde6e29ebe7d6eaf5120f959e80a`  
		Last Modified: Fri, 10 Oct 2025 04:54:07 GMT  
		Size: 94.2 MB (94151704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cab23bd8d05432762741acf27bf0b59895c6dc9a101fb344870543d4c9310c0`  
		Last Modified: Fri, 10 Oct 2025 04:54:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:472848eb0ba1b0deb41b53bcdcc9e889307c2785781de61761c91fb5775cff4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d055a7b8f67179b8adb0c7acb48b38a42953e17123eebfb623f1472b7c56b735`

```dockerfile
```

-	Layers:
	-	`sha256:a190d8211de5930cbed57dfec1b293eff27f15ef0c2ffd7e5e9f8b39df1d26b1`  
		Last Modified: Fri, 10 Oct 2025 06:53:00 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988617a84b68e903697c3beac122110c1628217af213c74fb80117e6672456f4`  
		Last Modified: Fri, 10 Oct 2025 06:53:01 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
