<script lang="ts">
  // initialise a variable for the select
  let selected;

  // array of subjects
  type subjectsType = [
    {
      label: string;
      title: string;
      selected: boolean;
    },
    {
      label: string;
      title: string;
      selected: boolean;
    },
    {
      label: string;
      title: string;
      selected: boolean;
    },
    {
      label: string;
      title: string;
      selected: boolean;
    },
    {
      label: string;
      title: string;
      selected: boolean;
    }
  ];

  let subjects: subjectsType = [
    {
      label: "mathematics-grade",
      title: "Mathematics",
      selected,
    },
    {
      label: "english-grade",
      title: "English",
      selected,
    },
    {
      label: "other-subject-grade",
      title: "Other Subjects Offered",
      selected,
    },
    {
      label: "other-subject-grade1",
      title: "Other Subjects Offered",
      selected,
    },
    {
      label: "other-subject-grade2",
      title: "Other Subjects Offered",
      selected,
    },
  ];

  // array of grades
  type gradesValuetype = [
    {
      grade: string;
      value: number;
    },
    {
      grade: string;
      value: number;
    },
    {
      grade: string;
      value: number;
    },
    {
      grade: string;
      value: number;
    },
    {
      grade: string;
      value: number;
    },
    {
      grade: string;
      value: number;
    }
  ];

  let gradeValues: gradesValuetype = [
    {
      grade: "A1",
      value: 4,
    },
    {
      grade: "B2",
      value: 3.6,
    },
    {
      grade: "B3",
      value: 3.2,
    },
    {
      grade: "C4",
      value: 2.8,
    },
    {
      grade: "C5",
      value: 2.4,
    },
    {
      grade: "C6",
      value: 2,
    },
  ];

  // sum function
  export const sum = (...values: number[]): number => {
    let total: number = 0;

    for (const value of values) {
      total += value;
    }

    return total;
  };

  function getGradePoint(grade: string): number {
    return gradeValues.values[grade];
  }

  const gradePoints = [];
  for (let resultValues of subjects) {
    const grade: any = gradeValues.values;

    gradePoints.push(getGradePoint(grade));
  }

  console.log(gradePoints);
</script>

<!-- O-LEVEL RESULT -->
<div id="o-level">
  <!-- svelte-ignore a11y-label-has-associated-control -->
  <label>O-Level Grade: </label>
  <div id="waec-result">
    {#each subjects as subject}
      <div>
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label for={subject.label}>{subject.title}: </label>
        <select id={subject.label} bind:value={subject.selected} required>
          {#each gradeValues as gradeValue}
            <option value={gradeValue.value}>{gradeValue.grade}</option>
          {/each}
        </select>
      </div>
    {/each}
  </div>
</div>
