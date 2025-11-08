## `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:4262f7ee56dcb60f434d635ee3b587409ee9c73228aedf6846c0d4e09f16ec14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:aa3e36bc0fb3ded43f50301eb9f19c4d1f941c7380b6ad339fd7c29b3dfc9ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156506552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149fecdf7fd3f607315ec0ada209fde04879df4aaa79f5d257a60ac20f8ae389`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:04:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:04:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:04:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:04:23 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:04:23 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:04:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:04:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:04:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387e295d53b6f92131397ce059915a5da0ae97f9d18c414fc814417a09b21ec9`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 54.7 MB (54733343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f5c2246a1b9812f65798049507066cf9528cd42d993180fc047f234c8e6ef`  
		Last Modified: Sat, 08 Nov 2025 18:05:12 GMT  
		Size: 72.0 MB (71994458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982aefc4c217c3c13880f83c8576a153351b51984aa61486ef1240a9958c7987`  
		Last Modified: Sat, 08 Nov 2025 18:05:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18d4186057b2461bff673831edc3684d7f37d0d79c167b4d11fe9133fbf042c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a2ed0cce54c7fac217ff120c71258de639bd9a5a3770bfab6c2413726b8edb`

```dockerfile
```

-	Layers:
	-	`sha256:066c4a173f6aa421dd931bab348f62f659ff8e99efc9020c002c52df0207bbb5`  
		Last Modified: Sat, 08 Nov 2025 19:40:38 GMT  
		Size: 5.4 MB (5377777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d85a9de49c3e29e295f47e1038a608749d32471587b9442224da0bcd12b6b7b`  
		Last Modified: Sat, 08 Nov 2025 19:40:38 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d29359f719a23d88f8e611047db30e019bec041b6f15dd83094a6f44919fb729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155766376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b5ea16c390e9037075da5d8a3aac1150b6363cabf343f6edbfabf497a34ee5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:03:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:03:39 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:03:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:03:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:03:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd82a615af06fc5ac14e29178d26bd56eb6df345c455519b74b733c665cbc45`  
		Last Modified: Sat, 08 Nov 2025 18:04:26 GMT  
		Size: 53.8 MB (53815029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36659050ea5cdea9c2983ec343811e76a81f64cf9b6672b475675e69a4ac8421`  
		Last Modified: Sat, 08 Nov 2025 18:04:26 GMT  
		Size: 71.8 MB (71808404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508b843b593c6b612ecd614eea24ee859582b08a2f626b4c36ba92631c49ef3`  
		Last Modified: Sat, 08 Nov 2025 18:04:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa912717240bbd180b14d75915a28afef915690e320a0350837fc7e2ecbf387c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a9113cbdf1a49d24cdf8671f8cfc1e3a388b7e08a51ed707b160508521e7b4`

```dockerfile
```

-	Layers:
	-	`sha256:c9063501dc7f3e8eae8960f6b484eed12a3461c6ea28138ff442dc0d8c277373`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 5.4 MB (5384244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a7bed5c595c6627ee6dbf87cd5eb799144a1a91aba3dc9bcdab3abd723f9129`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

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
