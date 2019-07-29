# sfx-java-agent-nonfinal-bp


Manifest exemple:

`applications:
- name: signalfx-auto-instrument
  path: target/greeting-service-auto-instrument-0.0.1-SNAPSHOT.jar
  buildpacks:
   - https://github.com/rhardt-pivotal/sfx-java-agent-nonfinal-bp
   - https://github.com/cloudfoundry/java-buildpack.git
  env:
    SFX_AUTH_TOKEN: _SFX_ACCESS_TOKEN_
    SFX_AGENT_LOC: https://repo1.maven.org/maven2/com/signalfx/public/signalfx-java-agent/0.28.0-sfx0/signalfx-java-agent-0.28.0-sfx0-unbundled.jar
    JAVA_OPTS: "-javaagent:../deps/0/signalfx-java-agent.jar"
    SIGNALFX_ENDPOINT_URL: https://ingest.eu0.signalfx.com/v1/trace
    SIGNALFX_SERVICE_NAME: jlr-java-pcf`
