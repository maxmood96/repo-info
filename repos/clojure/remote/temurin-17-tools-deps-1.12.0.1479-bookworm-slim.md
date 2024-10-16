## `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:659f2024df9980c4c6916f0c352f5290c38cd3e2b308ad4fa000a74463147674
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:be591bb29b9ae7dbfc192bc65827d21dedb483d742959cbcf1845038769c63a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243776398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9f40dfaab5086657488b793d141dba38b824a20d927f08984db8fa9a104e13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf181b1d0025d566f20d1913a51aba09065deb2390590d7080437237b8655e`  
		Last Modified: Wed, 16 Oct 2024 16:13:14 GMT  
		Size: 145.2 MB (145166561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f0afcbf2e1f9592a9452a21a960aebde3e2ef3cbc22159fa85a60ca800b6b5`  
		Last Modified: Wed, 16 Oct 2024 16:13:14 GMT  
		Size: 69.5 MB (69482516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f98747799d6984a228cb7a44b9aca6c5ae357fc42726314eaaf1a052c0ad737`  
		Last Modified: Wed, 16 Oct 2024 16:13:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210105deb93f64ff5f47096f36f8246bc4d592aecc937c327251100d988e0912`  
		Last Modified: Wed, 16 Oct 2024 16:13:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e8091f1f9c26255c8bf1edeca9e56fc3f267dc98b3e39258939818a8e07101a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4909726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e07ce693acb48acff29337dec450e37e00edb298c680bbc41d019bb0da12903`

```dockerfile
```

-	Layers:
	-	`sha256:97ce8f15c158f3483beda515c4c54632d840d1d289b2ca33da6d831bd442865d`  
		Last Modified: Wed, 16 Oct 2024 16:13:11 GMT  
		Size: 4.9 MB (4894211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a255636c1cbb15bb34e144554f636b7fb9419ef50b28d2ee0c68249c06413a`  
		Last Modified: Wed, 16 Oct 2024 16:13:10 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85e8a571681061c4675a0d03eee23c02f996e559a770b98f139f9eb0a4056e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242461898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edea6f11a85511f421788b0e84a34dd56f55c7b5badacab53d3678377798e6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72774100bcf4e6beed65977d9f3a42e818d1ab09eb70bceaa147e7dedd017c5`  
		Last Modified: Wed, 16 Oct 2024 02:22:01 GMT  
		Size: 144.0 MB (143959466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15cfd75919ab97a362acbdfc3e92efe193a53f0f6f1149e9dad398c5aa99225`  
		Last Modified: Wed, 16 Oct 2024 02:28:17 GMT  
		Size: 69.3 MB (69345022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e263a5cc0a13c20a986ab2299c4d9a18d4468f76d8868b430b11eacd5faa418a`  
		Last Modified: Wed, 16 Oct 2024 02:28:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0636fe81522ce0f15f112c0b3bd1f23eac92eacc7d2ef2efbfd4f5cf245cdf`  
		Last Modified: Wed, 16 Oct 2024 02:28:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99bb62c0f433a9e89d7046f32abeb9ef627682bc30ed9b228e09f7e520516c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7883a0da5eca10269b9e089c162543cf7d0bf0c6e40e30b154ee881ac3bba9`

```dockerfile
```

-	Layers:
	-	`sha256:fa6d9efb86953a16f3589c850592dec17e5f11e47e7f7df395fbfeec8845f3a3`  
		Last Modified: Wed, 16 Oct 2024 02:28:16 GMT  
		Size: 4.9 MB (4899977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86acf0a60661c17d69f126126a0eb1afcb20524a4cd076b30219cbff29506d3e`  
		Last Modified: Wed, 16 Oct 2024 02:28:15 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json
