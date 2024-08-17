## `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim`

```console
$ docker pull clojure@sha256:083cbeb275de5501cf76a3e4dbc2aa7ecf9608ddb3744cb2f0a11796b91a08fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:de3bc33b50f7b53f540a4af71c793be28a72b2077dfa059fd390a4a46a506e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235166188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c22f725979e29606fdcef0bfc85f9082786d4ed1507598f1635a9bed5aa1fa8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196aa1d5898a3068e020641ae927b0e33ba03ada362715c2d8f68ae0377ce3a1`  
		Last Modified: Sat, 17 Aug 2024 01:59:44 GMT  
		Size: 145.2 MB (145164850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccee3b834695cf8357cb0b64ca8e658e3c350a035813636b13bfe4e75738e78f`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 58.6 MB (58572009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69ceaea40b6c6fcf45670e4c0fc898c2b647d5597a3e39a42a5c92b2e5fe7f4`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a4f44f90fa6f4cb50fd32cd05ab2df52e309d309e5b01b930681fbdcee665b`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9fd42029f93b5129c91bc76fcba01e3feec90d5b586a7c82d6b8ba10074719ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7813020dd59a1694b536979309b4cd07ed0603e9ed4bf13f50e7a915b39c8e`

```dockerfile
```

-	Layers:
	-	`sha256:ff8f9a9d4ac77f653752664ac027f50ef26d0eab552277d94d67d69c07b2b5e4`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7f01f84357c8b1592c6f779aed84bd99f27bccd752962f24cbdb38ffc99c0f`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5aafeb456b3e6c65405bbbde948c4e468de04a24e0b3b6b2c15bd8945cf752b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232735840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4abaadf98cdb8e1bbe76d822fbe2cfa2c363f113e630432e5f03c9385a85dd7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e77718461fce3137ffc528beac77db0246cb0b5c93b3e3b0fe3e760c7ec7414`  
		Last Modified: Tue, 13 Aug 2024 06:33:53 GMT  
		Size: 144.0 MB (143959484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4af658bb5e68e5e6a1eb693b8da0332eef167445df743967fa9338fadf95574`  
		Last Modified: Tue, 13 Aug 2024 06:37:02 GMT  
		Size: 58.7 MB (58699231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2be6cbec80a753418bfca6d0959325a5eb3fa202204d9f8379b825d0d200d2e`  
		Last Modified: Tue, 13 Aug 2024 06:36:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0bb9ff7741611a4aaa1e1e75a1b0c1b3408d722cd51e95eb36176d0c4161fb`  
		Last Modified: Tue, 13 Aug 2024 06:36:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e50e2331d43967f97715a61069af2d61feae2410fc65437efb8ef85e9f8c757c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1ad2c2cf5373b3af2f7d0b63d70b0f59f2f8ce8ab8dc9434b3d4f322983a85`

```dockerfile
```

-	Layers:
	-	`sha256:468139c6764a808979ba996f0db16646f648405e2ac7047f323490c621e447e0`  
		Last Modified: Tue, 13 Aug 2024 06:37:00 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83010873373745c5cd26111e07bab7f3acfe3de16afb3d5573a0e9594c6e7cb`  
		Last Modified: Tue, 13 Aug 2024 06:36:59 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
