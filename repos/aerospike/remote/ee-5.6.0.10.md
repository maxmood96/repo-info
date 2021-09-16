## `aerospike:ee-5.6.0.10`

```console
$ docker pull aerospike@sha256:794c25e2962616db4dd2debd243f343a21aa12ac3b1563ad4abddaa2533e034f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.6.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:73ad3729ce0c81483b03383f4ff3c4a628c04f31202a55ccdbbdccfbe7882fbe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82472450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8861338182282af08755430ffc85d17bb5d129397f0e3f7b5717d6882b62ab3f`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Thu, 16 Sep 2021 19:19:22 GMT
ENV AEROSPIKE_VERSION=5.6.0.10
# Thu, 16 Sep 2021 19:19:23 GMT
ENV AEROSPIKE_SHA256=b667ff95e03b82f6aab6e965c4a315f856b56c7d60a42139423446f95b56c5e7
# Thu, 16 Sep 2021 19:19:43 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 16 Sep 2021 19:19:44 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Thu, 16 Sep 2021 19:19:44 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Thu, 16 Sep 2021 19:19:44 GMT
EXPOSE 3000 3001 3002
# Thu, 16 Sep 2021 19:19:44 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 16 Sep 2021 19:19:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afb3fc9286154b9aa0f5e2f1ec4f0f94e3e987b90975ecf9d3cd8879903c00a`  
		Last Modified: Thu, 16 Sep 2021 19:20:27 GMT  
		Size: 55.3 MB (55324522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261739e8ac716d21d55edc6ceee9a5e91dbce5cc2694319c7f380f159961e4b4`  
		Last Modified: Thu, 16 Sep 2021 19:20:19 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5472022cbe125bc0c4fb9e767a000f7a8f070c250b2c7e42792d56b8351749a`  
		Last Modified: Thu, 16 Sep 2021 19:20:19 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
