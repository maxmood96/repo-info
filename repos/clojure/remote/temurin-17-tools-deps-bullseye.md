## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:841ce499761adba0bb1aff84b8ff9c7adc92a57440660fe780033bde4124a81b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:89d991c32f92295a565c48f469b6ae4fd85e1edfaf4c2fd1ea15149dfaed2ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267711122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c7d1423babb6c41417790ecc7f7a7970e4f8b7b04fa633440ec8b5b7467b93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a70ec081fbe5483487a649b2193a32f747c470c27017d713f7d66bffe2e87f7`  
		Last Modified: Wed, 09 Apr 2025 02:19:00 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05168e70ea5848c53b9c64561195fa0520c900df163b2ee4fa6e98b9dc414389`  
		Last Modified: Wed, 09 Apr 2025 02:18:59 GMT  
		Size: 69.4 MB (69395025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831a553bc64e65eb412f2d6443e3f265d24b34a40d0b8e3e32e9ebff7656e29b`  
		Last Modified: Wed, 09 Apr 2025 02:18:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6bf15979fa79dc9e4b693b2deebb7fb9c10b2b7ee31b5d29a9eb852f32a7b0`  
		Last Modified: Wed, 09 Apr 2025 02:18:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:327706a2447bb68371e7edb5e06ac178bd1e4e1e89af43156caa63395f9e8bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e315772660fe8f61aa53e74e95bbaac2b2199dbee3242f499564a67f0e279e9d`

```dockerfile
```

-	Layers:
	-	`sha256:08574b10e30ef8289cb53f06b4465364542aaf6864ff45dcc70894548a9f0e4b`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 7.2 MB (7206501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c9b61f73d82f7415269b4c2637f0fc2b9abe111852a1cc8df3f69957b84be0`  
		Last Modified: Wed, 09 Apr 2025 02:18:57 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eea80442ff5d10a2dfb1d00b92f4bb59ca13ed9a633407f63a0932323912e644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265239557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20685ec849506659bb9ebf993658cb4333c2c330182984f8360c731ae26ce4d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b78c9a7099b2ef01571f7d5b8b18d1fb930e46001fa81052be0bea3123bdfdf`  
		Last Modified: Tue, 08 Apr 2025 11:27:21 GMT  
		Size: 143.5 MB (143454701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca10eb03135f69bc07f848aab81855cfe2e8e5606d3682ada89057abc48662a8`  
		Last Modified: Tue, 08 Apr 2025 11:30:19 GMT  
		Size: 69.5 MB (69529591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9a033b46c4586d25beccf5af93fa2d4ffb84631bec3b63855197b79910cfdb`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586311341a03374716532bf3c8629c5e1ca2acc95319504539475cd5de61bd0a`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d144cd8389a05fae26d6036b3fdfccf50f2886c2cb381f9be3b5af9009891e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86aabae43f6ef334d9fd16a2d4af9fe7c93d3c2f789eafc57d1683ec0f21233`

```dockerfile
```

-	Layers:
	-	`sha256:71d3951b402603a975dcb139602838e27c7c477ef2e546b060841b480558b527`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 7.2 MB (7211600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883f53f29b048d3a28e2742d8429bf22e569b52c4666ec4975efc26c05cbf4d7`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
