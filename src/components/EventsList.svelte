<script>
  import { Col, Container, Row } from "sveltestrap";
  import { EventsListStrings } from "./Strings";
  import Modal from "./Modal.svelte";
  import DressCode from "./DressCode.svelte";
  const {
    TITLE,
    DRESS_CODE,
    CEREMONY,
    COCKTAIL,
    DINNER,
    DANCE
  } = EventsListStrings;
  const columns = [[CEREMONY, COCKTAIL], [DINNER, DANCE]];
</script>



<Container id="events" class="text-white text-center">
  <Row>
    <Col>
      <h3 class="mb-4">{TITLE}</h3>
    </Col>
  </Row>
  <Row class="events">
    {#each columns as column}
      <Col>
        {#each column as { TITLE, TIME, DESCRIPTION }}
          <div>
            <h5>{TITLE}</h5>
            <h6>{TIME}</h6>
            <p>{DESCRIPTION}</p>
          </div>
        {/each}
      </Col>
    {/each}
  </Row>
  <Row>
    <Col class="text-center my-5">
      <Modal>
        <DressCode buttonText={DRESS_CODE.TITLE} message={DRESS_CODE} />
      </Modal>
    </Col>
  </Row>
</Container>
