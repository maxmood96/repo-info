## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:560de309883d7e4a714e2965e126b23f32902a7e39f9104365194895846a4370
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d5ae68a80887500d5b7b530b10c12c1f4f792de91a4e354b45f56ee4bf0b2df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156505328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc61e48bb324aaec7bab802903ff51f6000c5bdff526f299b3f3ec50a2406fc2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:29:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:29:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:29:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:29:59 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:30:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:30:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74f3e5b4594572705b68907d0a0209eeccdc9b57e0f95bd36f37cbce1583562`  
		Last Modified: Tue, 04 Nov 2025 04:30:51 GMT  
		Size: 54.7 MB (54731322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4206f6ca8c0918a7873e81eb3116b38aaff53bf1047a022b5a8ca8dc0d15284f`  
		Last Modified: Tue, 04 Nov 2025 04:30:46 GMT  
		Size: 72.0 MB (71995259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467f1743ceac9954bd172ee95c4fa03091869f7f3f262409f7d0adba90023e6c`  
		Last Modified: Tue, 04 Nov 2025 04:30:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b75f16f3f158c9c1b18e2453445170065eeddef084cfd48fd557bb207f1d3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407f79a3dccd69e87b474a90ec5a620d0f708c259a270e440f483640d529310d`

```dockerfile
```

-	Layers:
	-	`sha256:b6bb1e5cd796aadccc6dfa1f59ac3f9c6ed9d1c563b2e1917c3cbe1f9f67f0b2`  
		Last Modified: Tue, 04 Nov 2025 10:49:37 GMT  
		Size: 5.4 MB (5377777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30ddd9715a516bc79db833dbc0ca3ceb33a31e330eb0a1f90e6b6d1adcebb38`  
		Last Modified: Tue, 04 Nov 2025 10:49:37 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aeccb23bd18c5a247f11bc2860e81f8940cbcf502c77ff40456aa6e683f685d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155786781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c8476ba20edf91298f241210ef1abeb245306d4fee71a6fe80ba37e5b56a75`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:43:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:43:37 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:43:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:43:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:43:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35637ca6f704d3cbfde36aeba4df9be0f4bc618541dac495c39a0f9159a652fe`  
		Last Modified: Tue, 04 Nov 2025 01:44:32 GMT  
		Size: 53.8 MB (53835577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca940beb280db7dfe033a70c8719ebb99591e2649e251a3cffdd25e72ec6937e`  
		Last Modified: Tue, 04 Nov 2025 01:44:33 GMT  
		Size: 71.8 MB (71808262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7cfb5c5baa80c4ade2f232900530c4ee6aa1e976978f0757ed907fd9f8cac`  
		Last Modified: Tue, 04 Nov 2025 01:44:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13d6cea09e8308c2c0e7149688f19b0d384513f579485cbba83399a689e942a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76b91df08d07a9bc5df568d974a25019add27f301c7d8dd24e3c2a943e417a1`

```dockerfile
```

-	Layers:
	-	`sha256:18690a4ac566220e628542106e1f74b823276768519d6d0e11e45debee0f687d`  
		Last Modified: Tue, 04 Nov 2025 10:49:42 GMT  
		Size: 5.4 MB (5384244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d29a135c83d1cfd1395eba715080f696a35e975c026af306e96474eb789d5e`  
		Last Modified: Tue, 04 Nov 2025 10:49:43 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e7f044d4a90d82f89564304a714c9baec53b1c75bcc9d3f4126159cef174099f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163161817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a9a9617806667823afce12dee97bfbdebee505fd4a44a5c964e942f552f59e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:04:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:04:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:04:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:04:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:04:05 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:10:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:10:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:10:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1238aaaad8882076b4c982f227415c87f083a64c6a1006f173b38c1418642696`  
		Last Modified: Tue, 04 Nov 2025 13:05:25 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada7d188f4804dda26e50238dc06d64b853c405ba8bcaf5b324dbdfef394d472`  
		Last Modified: Tue, 04 Nov 2025 13:11:10 GMT  
		Size: 77.4 MB (77397154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d4e286191f11bcc714a80237be7f084a8c97f06decf5af3d92daae38184c5b`  
		Last Modified: Tue, 04 Nov 2025 13:11:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:798d2b5a5dba72d2f1db054c283916150790d9890014a9d31b24039279de8df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef91d1a91b5c7817354f1845803b7b485a404032c78dd8166e8575b43f9664a`

```dockerfile
```

-	Layers:
	-	`sha256:a8f61b711c69f0f769e1834449aec8d4f4882beb8aeec82ddd33e37a0179bb1e`  
		Last Modified: Tue, 04 Nov 2025 16:41:18 GMT  
		Size: 5.4 MB (5382741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279c366f22a927b9039a0503071b787faf2a12d1543206e3c3c49e1ab4771a2c`  
		Last Modified: Tue, 04 Nov 2025 16:41:19 GMT  
		Size: 13.5 KB (13476 bytes)  
		MIME: application/vnd.in-toto+json
