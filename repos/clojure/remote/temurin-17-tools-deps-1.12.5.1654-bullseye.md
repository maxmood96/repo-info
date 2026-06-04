## `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye`

```console
$ docker pull clojure@sha256:060f83d7da584600874cfdb2a1ab2b617ebab8db7a8abd60baa1fa0a647900b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:58b4782a42baaf096381062351bb7d721865fd79d66188939e5b33e40b6b2cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266187649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777ab50028b94497eed7a26f30ffa4e8eed43039c3311cdc35d7ffbdce7d8d46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:51 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf536f639dbbc3aa495012bb87f5de5bd2c5e67711bd6c6c9fe2e182d67396b9`  
		Last Modified: Thu, 04 Jun 2026 17:46:29 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca92bb1cb4ba770fde27a5c45e79bb246d15935307c59c202c812e8dc9a74d36`  
		Last Modified: Thu, 04 Jun 2026 17:46:27 GMT  
		Size: 66.5 MB (66512309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3aeb0ccbf38e824e7995a96b6ffeab1189575b10c3c8e5b76b689effff8b9`  
		Last Modified: Thu, 04 Jun 2026 17:46:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8af9c2cc0a419f369ff103e5dc740cc136cfdcabb17719e4bfecf9332238c8`  
		Last Modified: Thu, 04 Jun 2026 17:46:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:521c3c3cbfe021ad5ec856c922abf138899a520ce9a0d6dfa941d1cd1a20ce5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ab7253916dfefbc2c43a5a273cf850cd4584e5e18b3383977507fa1fec1e77`

```dockerfile
```

-	Layers:
	-	`sha256:d4aa749c0ee23e93be8874e32a9c2f9e15e8af957b6ad959bcab2f7b4c545cc6`  
		Last Modified: Thu, 04 Jun 2026 17:46:24 GMT  
		Size: 7.4 MB (7405445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f5fd5459af3807facb11e7899eea227d80b6441a28dc4106d03b5ad2c565f4`  
		Last Modified: Thu, 04 Jun 2026 17:46:23 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:734be82b244ee043badca63b27348f2a7333d839c7e2cb6829a495ad0960dea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263659833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5789590e19c65e5aced88441283742f2f184041c1e694dac8293ebf9e6d9dd35`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:45:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:42 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eec7eef0b8676c7aa0f22c3e72bba509d10ecad0d4e1870ef660222f3d9471a`  
		Last Modified: Thu, 04 Jun 2026 17:46:20 GMT  
		Size: 144.7 MB (144724361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2657be03187403ad7ee115b6450047e84d90169f3a551fa5045c0d3fd98e4f`  
		Last Modified: Thu, 04 Jun 2026 17:46:18 GMT  
		Size: 66.7 MB (66677849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d88ee0150df282bd24d3ce8e6f832ae8bb0f092422ffde2d2d29de12ccf9e58`  
		Last Modified: Thu, 04 Jun 2026 17:46:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf88adb75c1e460b5a69806647224875a3ddde197402b1ec2766edbddaabb7ee`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:072674b6a6f30bcda32a62ae8dd84fabe6f8e9e775ef6a6689dd46ee7fd2a32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f99a3978b2b14fa1099e3cf84bcd64653be201a710652ed99bc63405fc50744`

```dockerfile
```

-	Layers:
	-	`sha256:9c8bf323ef83bf99a48264fd6552168cf426f1d5988ef29dd398f27bf45042be`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 7.4 MB (7410544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049be186ac98bc9d4210201ceef5208bb5759b92c7ef5df16fbe83702d7eb1c4`  
		Last Modified: Thu, 04 Jun 2026 17:46:14 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
