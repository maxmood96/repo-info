## `aerospike:ce-6.0.0.1`

```console
$ docker pull aerospike@sha256:5aba25bfd33c1e4183e14be824a44a1422f7ba778f46ce592e808a849187d6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:f38a0755ae6c0c791805f62d50ff70ca8d32f05f457cbc2b50e4954cd2259cae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100929189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2277a1edc5d8445aa5977b93214794c43b5f310460b34c503674a07874ee3696`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Thu, 05 May 2022 18:19:19 GMT
ENV AEROSPIKE_VERSION=6.0.0.1
# Thu, 05 May 2022 18:19:46 GMT
ENV AEROSPIKE_SHA256=79aa40b1028798b5f13e23f295c1e1af187419b9410e23ebb692e350286fac5a
# Thu, 05 May 2022 18:20:06 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 05 May 2022 18:20:06 GMT
COPY file:57aa54f8d05380c639ff298f99e0387bafe493553aa29e39911c8342f60a0f0e in /etc/aerospike/aerospike.template.conf 
# Thu, 05 May 2022 18:20:06 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Thu, 05 May 2022 18:20:07 GMT
EXPOSE 3000 3001 3002
# Thu, 05 May 2022 18:20:07 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 05 May 2022 18:20:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff5bcfddc6e7816f561ba1dee874e40f12829cd8a0025c8385293bacba846fa`  
		Last Modified: Thu, 05 May 2022 18:20:42 GMT  
		Size: 73.8 MB (73786494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bf5f9a02f6f15d5134a4a685da6730d952381292faa2e9f3412a2d96d6824d`  
		Last Modified: Thu, 05 May 2022 18:20:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cf52df95f75f9702900e963281cc1f97fb2d89403a81318230c3c914683b11`  
		Last Modified: Thu, 05 May 2022 18:20:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
