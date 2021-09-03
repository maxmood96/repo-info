## `aerospike:ee-5.6.0.9`

```console
$ docker pull aerospike@sha256:7a9d9588f73384dced51aee56b94563192339510d04e0a0464f007550b2ed950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.6.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:9e1f6f753ea7eed14c4203f83416b1121ffbcf8cd37a62812cfc98e0eccd48d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82472465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa526f6cf22249f709b0e845393f43c5a79cdd1905c78d99dbe3bc7fe170d86`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:30:58 GMT
ENV AEROSPIKE_VERSION=5.6.0.9
# Fri, 03 Sep 2021 03:30:58 GMT
ENV AEROSPIKE_SHA256=c7b16a194bc6a025b7f97f962a4102da255c38bdf99ff59bea15349be3bd02cb
# Fri, 03 Sep 2021 03:31:35 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 03 Sep 2021 03:31:36 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Fri, 03 Sep 2021 03:31:37 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Fri, 03 Sep 2021 03:31:37 GMT
EXPOSE 3000 3001 3002
# Fri, 03 Sep 2021 03:31:37 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 03 Sep 2021 03:31:38 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbdf2d87f7b7584523e1349ec0d4b188d0a96a3543be4d49306e8f20918886c`  
		Last Modified: Fri, 03 Sep 2021 03:32:34 GMT  
		Size: 55.3 MB (55324539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bf41abf901807a14b23d4b93916b9556db7f276c32058045fec3edd81d7708`  
		Last Modified: Fri, 03 Sep 2021 03:32:24 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa189d3e88af1c40e023a1479a6301b465e8e2f0604e8d28fc2c83a5041ba7a`  
		Last Modified: Fri, 03 Sep 2021 03:32:24 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
