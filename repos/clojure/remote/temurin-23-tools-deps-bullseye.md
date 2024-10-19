## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:8987e2cc24790ff724a90c173ebfce886c8a47c42ff68618322f9d4329edde40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1476d4fc0cf7bb3afed7d82f6586e6c5e8f65f6c8558eb6a4c0dd4cbfaadc506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289683201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1941ca9b55fc2a41566cf62493e5a6adc71617b8eb1de3b5b1de9c786a1dd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038405483b0a74cfddef48c78d7dcbbc54d03b2cbf234706218410a85be15e71`  
		Last Modified: Sat, 19 Oct 2024 04:06:54 GMT  
		Size: 165.3 MB (165267642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a62d9881c7f90be0d2a8d341b1bc7a99b7b940ce8b78ddf06045c186dbd2de`  
		Last Modified: Sat, 19 Oct 2024 04:06:53 GMT  
		Size: 69.3 MB (69333910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9daf425365b56576245c562591ac9f1886f9511a1873aabb60c55211796736`  
		Last Modified: Sat, 19 Oct 2024 04:06:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b17a5ca7957faeb2ecd77c87723d4824455fe645cd09f3443657c1a73e1fe10`  
		Last Modified: Sat, 19 Oct 2024 04:06:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bae9e87f60250b5262c552fbbf134d1ac4237a2eaf2c4372b5677182d88f5e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37118c154be48514e57809b59f995e61b4227ee5de4932fd462b3cf0158c948`

```dockerfile
```

-	Layers:
	-	`sha256:83a31a12fe544cf28bff9f3e325a29416d32f5ea073f9f2799a73db3e4a6c31f`  
		Last Modified: Sat, 19 Oct 2024 04:06:52 GMT  
		Size: 7.2 MB (7220831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752482cd43a8a78bc212e6e97b33ee881267a3b09789f31dd9953e37cb8ccf4d`  
		Last Modified: Sat, 19 Oct 2024 04:06:52 GMT  
		Size: 15.6 KB (15645 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f58d6eb0c91e8ecc82fdb03f8f502f49497d118db79e1069779985e27932308e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286455660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba2d4b5226671c7095b2ab155dd6093085523e72a6b8641a05d6e77c63ce538`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e3acd407382ba38be4751d630a7d727bf3b7c34f0761ee6972cc6a0d9947b0`  
		Last Modified: Thu, 17 Oct 2024 08:29:57 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb74ca72c72562f7df25601c768ceedb917c24fc75e71697f0be9c5fa72a1746`  
		Last Modified: Thu, 17 Oct 2024 08:34:14 GMT  
		Size: 69.5 MB (69466925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f5cdb7ea85c7b78d28ed4315ca5d3de5b3f202146f830d75c3d4b4508a12d`  
		Last Modified: Thu, 17 Oct 2024 08:34:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8cc0b325b8497bd2ccce895b6000f96e8b8c7e95f6e67adbf877a1e9edb8c1`  
		Last Modified: Thu, 17 Oct 2024 08:34:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1478a59721d182dafbeb4243dc6ca297cacfe2aa64356761ad907ef4a27b89d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7ca0d6638452a680b8057195d7b2ea37e86fb6a04c4254f377a2afd0b58a20`

```dockerfile
```

-	Layers:
	-	`sha256:a3916478bffba3e5e3b5ab178bffe403b353f4af49ffb35653214d35927ea683`  
		Last Modified: Sat, 19 Oct 2024 12:23:13 GMT  
		Size: 7.2 MB (7225312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8fab135e139f3be9266fbcf4585d0251694332cd3ddcc979043498674ae886`  
		Last Modified: Sat, 19 Oct 2024 12:23:13 GMT  
		Size: 15.8 KB (15756 bytes)  
		MIME: application/vnd.in-toto+json
