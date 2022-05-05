## `aerospike:ee-6.0.0.1`

```console
$ docker pull aerospike@sha256:dc4d40be75a7b955d8084eb0bcb3a2ad08812c233f41edb78311a2d3c83d493b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.0.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:9d127ed1d0766f50fa5f2efe1e7b9bcd150e2448d1854be542a888ce784a09fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103321598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17869b631607a050f86f620603102689bc14dcee26f902773726bcd1833864f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Thu, 05 May 2022 18:19:19 GMT
ENV AEROSPIKE_VERSION=6.0.0.1
# Thu, 05 May 2022 18:19:19 GMT
ENV AEROSPIKE_SHA256=d470ca9717b563726e8084ab6fc89f2889aefd1f6aa8ef9145ac38e0b42945a1
# Thu, 05 May 2022 18:19:19 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Thu, 05 May 2022 18:19:40 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 05 May 2022 18:19:41 GMT
COPY file:fa3bf0bd6c8130f09c26d82e9992baa4f2fe9ac69fee03e01b296f89984a97e0 in /etc/aerospike/aerospike.template.conf 
# Thu, 05 May 2022 18:19:41 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Thu, 05 May 2022 18:19:41 GMT
EXPOSE 3000 3001 3002
# Thu, 05 May 2022 18:19:41 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 05 May 2022 18:19:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f4ce7940a33dfe75da39d3c609039a1ed026b798607715bf92357a32cef3f9`  
		Last Modified: Thu, 05 May 2022 18:20:24 GMT  
		Size: 76.2 MB (76178844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d8c2282aa6c904cb5cbe3a8174b60d5862255eb1eb4df040d01bd5a11a9102`  
		Last Modified: Thu, 05 May 2022 18:20:15 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3565162472c2325e474d8b75ec06099168f376a99608f0699a91e90ae383d78b`  
		Last Modified: Thu, 05 May 2022 18:20:15 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
