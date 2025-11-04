## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:f1114d21a739ef2d47b1f97a392aaae8543642e278acb33e1532bd77b47406e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3ef778a93e041b5325007d59f18501ccafbad1bca62ae1a592ebb000cb51f9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287433034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba224cbd31ac6b99ee4ff590d610bc308fd72ddcd283c726b985cefdab8a7ca9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:55:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:43 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7734c83a371733bb864682cd8d5d039e9fe3f1b2be0a2e7ca7d68a203d6f8111`  
		Last Modified: Tue, 04 Nov 2025 10:54:15 GMT  
		Size: 157.8 MB (157804741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75ad1f693ea4d6b91b6148af4b00497c3b84894532b271fa4d485479d762310`  
		Last Modified: Tue, 04 Nov 2025 00:56:39 GMT  
		Size: 81.1 MB (81146201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dbba4c53e53daa8a4a834009a83ded5bb77836dcc58f3e0ff168c2d897b926`  
		Last Modified: Tue, 04 Nov 2025 00:56:28 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed7ec3e3d9c0ab48996bacd2c6bb58c691d3aabb41e3174dc9762f16029f68`  
		Last Modified: Tue, 04 Nov 2025 00:56:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ff0e936fb0e0620ca26c2c9e3dfce23c79c72bdca2d16ce29eb7b6df90df8dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ad241ccea427ec222aab62e447a34584f778efd1ce53ccd16d884e20cc0d68`

```dockerfile
```

-	Layers:
	-	`sha256:0ce78239144642cf298c7960d145741570f60cc9fa7a35613e706ebe984fad04`  
		Last Modified: Tue, 04 Nov 2025 10:42:11 GMT  
		Size: 7.4 MB (7378676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68ee845454f439fa0f82431cfdd1dfed78f4c83df126d7a3c6969e3bdc6796ee`  
		Last Modified: Tue, 04 Nov 2025 10:42:12 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69de2616c988dbfe2289fe8ffef7a7f14ab53b56d59d6fe12e9d497773220134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285472823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a01ac0f35536e6ccda1b6eae36c3a978919157c5c909393ff2fb8e38937fc84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:56:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acda20b7ddbf9637314c51e32027fc23ceea930a5ac5c07bafc2db78475f7451`  
		Last Modified: Tue, 04 Nov 2025 11:06:32 GMT  
		Size: 156.1 MB (156081238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4344c434819f433d9d6241f147e19d868143287a3a8c752f5430e25617bd4`  
		Last Modified: Tue, 04 Nov 2025 00:57:32 GMT  
		Size: 81.0 MB (81031065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4fbc5e88150f971784ed2425492e7e7aa43ad2f30d2ee5d6752b79cbef1565`  
		Last Modified: Tue, 04 Nov 2025 00:57:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd4471d6ed4e2de65cc52e9047aba5b4d68975ecca61c0f970dc3cebc419ed1`  
		Last Modified: Tue, 04 Nov 2025 00:57:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a7ce7351b31f2ac939e593f18207a913e372a8f7b6791a9b9a8b43d4fd0efc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a435fdc640fee3afa170a21d30fccf2d1db28b5ea9ae1966afd27b80c8e91c`

```dockerfile
```

-	Layers:
	-	`sha256:dd60d7b45ea83d9595d67461c3d39cf8cae5a59712947f7574127cd7e4970b8e`  
		Last Modified: Tue, 04 Nov 2025 10:42:20 GMT  
		Size: 7.4 MB (7384463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a26b33b7c7ae8f82b8d72647562e2446a49837ecccdd4b0dfbe344f6b7e5424`  
		Last Modified: Tue, 04 Nov 2025 10:42:21 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1277fd727171105feb5a9fd85bd9c1bcbf4ed33184a6db9d8cdebf29b58d7483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297277734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe5aa597753faab1cc9717c481cfbff7a6505880f20d74232f5be4e78b049ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:30 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfed681a131059fef5f258e337944be0ad4a0ab0a0f864dd465487a2c1aa3a3`  
		Last Modified: Tue, 04 Nov 2025 11:07:07 GMT  
		Size: 158.0 MB (157963427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb548b38a0c256b8a6450a3cdcdf83c056392e2d4ccc8870eef442fa1f0ff6`  
		Last Modified: Tue, 04 Nov 2025 00:56:55 GMT  
		Size: 87.0 MB (86985984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216a73236e942b9fa3e09ac6c88ebe28ddd45f5e6d4c1977cdfd844d5fe2aa14`  
		Last Modified: Tue, 04 Nov 2025 00:56:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b38644bd241ced82f098c01778a8a890e006420e98aa17486e10bcbc9b027`  
		Last Modified: Tue, 04 Nov 2025 00:56:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d0580e5613f4879eac82c78521af9832cd3317a7b605d09ba157486024770c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc443ddd2695d0cc4b4ad4a25e7fd10c09d4219a49d9dd8a524efeeea6ccddcb`

```dockerfile
```

-	Layers:
	-	`sha256:0ce2d5ae1684364e226c15ff329854a02e379fe23aa882063746aab52b8962c2`  
		Last Modified: Tue, 04 Nov 2025 10:42:26 GMT  
		Size: 7.4 MB (7383902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb35e663d2628446edc6adb68692c18236287674b0f277ebd734036bb51d5a2`  
		Last Modified: Tue, 04 Nov 2025 10:42:27 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:96c6f69516ce89a52c9cb6e2a6c67ec44320a7b0b33d35ab7c889bc724b2d8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274122694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66faa987ef2c70c1d8dd92151f96d3bea30f714b1640a0b6a98185267cedb62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:29:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:29:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:29:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:29:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:29:41 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:31:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:32:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:32:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:32:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:32:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fde30b14cceb4c80b5871c74f0422e956b7c7142270a5d3a1d99ea678a172e`  
		Last Modified: Tue, 04 Nov 2025 11:07:42 GMT  
		Size: 147.0 MB (147026950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcef5869d0136bf70976c1a89e98973cf954dd8ff837d3dbe04f781184e873a`  
		Last Modified: Tue, 04 Nov 2025 06:32:40 GMT  
		Size: 80.0 MB (79956613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ff13a33d49f892b3017ec623ceb6bef06f7773e0638a6e9270157d0867227f`  
		Last Modified: Tue, 04 Nov 2025 06:32:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00604164ecc8ebcd8c52753455d22c8f6bdbe0f2b470db0eaf0b1ce9041955`  
		Last Modified: Tue, 04 Nov 2025 06:32:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:943ae6e39c06973cda5889dbdf4d7497dab50020e7707778ba6d13b222698db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a9c93cc077c015bb4d04b589dddbda93040e721bcbdebe52fdf670f12ebcdb`

```dockerfile
```

-	Layers:
	-	`sha256:c67f610816f3fa9571bc4dae548de116346a89428bb207b62fb454a3387f12ef`  
		Last Modified: Tue, 04 Nov 2025 10:44:21 GMT  
		Size: 7.4 MB (7369995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857c72866ffe4218cb113a06e7037801ea2207bc4f48ab9943551c358aa38098`  
		Last Modified: Tue, 04 Nov 2025 10:44:22 GMT  
		Size: 15.7 KB (15661 bytes)  
		MIME: application/vnd.in-toto+json
