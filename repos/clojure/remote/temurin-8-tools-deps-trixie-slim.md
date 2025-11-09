## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:df989d1e8ec4fd90089a2d9b351b5717695642480ca4ac6336ecd0c1a35076e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c7970f791055c4fa87b43b761bce8ae0afb8d53e110fabce0b41f164a786d4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163171474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efe3857a21a00c1dde09e0ca573eb81e911f6638bfac4bd39874256be36ce6c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:13:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:13:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:13:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:13:08 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:13:08 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:23:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:23:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:23:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0facc06cc8e166d71727a4983c45c13f2011e076102fa7c0cdfb760611832d`  
		Last Modified: Sat, 08 Nov 2025 19:15:06 GMT  
		Size: 52.2 MB (52175085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ccd3f21b4e6a8e67cf763980967bfdf356a4771ad8c1b7cde391f465cda25`  
		Last Modified: Sat, 08 Nov 2025 19:23:53 GMT  
		Size: 77.4 MB (77397095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14000c41b80ca275ce544b1b46588bf90aa393a1ceca3dff26673a8acdab26`  
		Last Modified: Sat, 08 Nov 2025 19:23:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f0b3507f5ccb713420d9fc4a4247d5873a69ec86d116c0449a885ff44e1cca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bbfff60e59b4b3969961c42accbda894a6262ad0d4b30e537b10ad784d0bcc`

```dockerfile
```

-	Layers:
	-	`sha256:506c6899243756115b6de94c03114073006a40f976915f7a6144979b7a5b628a`  
		Last Modified: Sat, 08 Nov 2025 22:55:44 GMT  
		Size: 5.4 MB (5382741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9b244f1df6259b697c628ee41b49fdfdd5f61c86687bb4f220d7ab4c10a13`  
		Last Modified: Sat, 08 Nov 2025 22:55:45 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
