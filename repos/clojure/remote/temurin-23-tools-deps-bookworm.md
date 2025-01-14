## `clojure:temurin-23-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:580e24104a9f66c35953196d5371bcda7986cd02a5b638dd4766c43138cda03d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d0a1a8fae97dab34442a29334a5199d2f7d9cb62543f51a97fec7034240204b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294754026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e22c1582af328275b0b7272c58b5157517e606aa81252efc975010a24a91a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d87d6b5eea6fe1b6251aa788e02b5d616b8840f59f515cd713472cdde82924b`  
		Last Modified: Tue, 14 Jan 2025 02:45:11 GMT  
		Size: 165.3 MB (165295104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28448277503f41d33af722e1417eac56da32cc770bc9fadf9b6ed8bb3ac6cb4`  
		Last Modified: Tue, 14 Jan 2025 02:45:10 GMT  
		Size: 81.0 MB (80977922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccd5a24f00cf290c7a3408296c9f4f07a04ac940f92050037b6e187f6972dc2`  
		Last Modified: Tue, 14 Jan 2025 02:45:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176b575766576e0bcd8c50fbb807967bdf759d1fb20195f8691b03aebfa8d3c4`  
		Last Modified: Tue, 14 Jan 2025 02:45:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:28ba77121e9619788c236acc7e932b8e28f077251c321531a2abea8799e42081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cffdbe8d134a520138b88515033032b73e4278b783ac0775fbb34c18b31f27`

```dockerfile
```

-	Layers:
	-	`sha256:dfea44a51c869b55f64d02f50d77d53fb91382ee36e7d2536c2cb3c73595971a`  
		Last Modified: Tue, 14 Jan 2025 02:45:09 GMT  
		Size: 7.2 MB (7176769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71dbf358810c88ce813b305d8c69d7c45852d0119a0d093f234ee80a5d93175a`  
		Last Modified: Tue, 14 Jan 2025 02:45:09 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44cd5f7fbd8208db78b65157d3859d08b3bbef977370c9d980e696bd276840cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292232241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2577667dde8bd8b9e037dc99f0cfa8b590da8348b927b56b8c6e338c63ab1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05182ce04270e6342718b72641c3eaee0e4fc79c31cbffebd00bee2cdf25c2e6`  
		Last Modified: Wed, 25 Dec 2024 07:37:03 GMT  
		Size: 163.3 MB (163281797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef775b5af65d4f4a5ad6c95b74d6a4163b000c43f472eadb921433226f6db3d3`  
		Last Modified: Tue, 07 Jan 2025 03:36:06 GMT  
		Size: 80.6 MB (80623921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23c4e3499b7c2701b73e57790d443f9aca96663beb02a6ec1565177f1d223f1`  
		Last Modified: Tue, 07 Jan 2025 03:36:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d8e50d52f344b167843d48474fd549f6486dd1c084a1a83b1a4bfaae9b25f1`  
		Last Modified: Tue, 07 Jan 2025 03:36:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:04d5522aae5bf88f18720ba9bbc9bdf99c440a8ce30b08a0158e43e2ce3b2ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bbb4bca1be5db75172ec364049b7e3d6bf1d2ccc4d7f39d5499f3524c4d79b`

```dockerfile
```

-	Layers:
	-	`sha256:ea04c09919bf907a04ed5b5c224ce34883d6ba2d6d485809ee19cb2ea22b5947`  
		Last Modified: Tue, 07 Jan 2025 03:36:04 GMT  
		Size: 7.2 MB (7181935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593da6542ac0f14515eff44504564b488734b0f1f0c3d6ffccb59263b78ccd63`  
		Last Modified: Tue, 07 Jan 2025 03:36:03 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
